# Projects

## Project roles
Each team must assign roles for all teammates. Each role is evaluated independently, thus number of roles per each teammate must be ~equal.

* Project planning: the student must describe (or gather with the team) a document with the following information:
	* Project name
	* Project scope (what algorithms will be implemented)
	* Project stack (what libraries will be used,  how the project will be integrated with other libraries)
	* A scheme of the project (no certain requirements for the format, but you can use IDEF or UML for better clarity if you want)
	* Present this plan
	* **Evaluation criterion:** presentation at Tech. meeting 1
  
* PoC. The student with this role must implement a simple code that works w.r.t. to the library structure/scheme on a simple benchmark.
	 * The goal of this activity is an early check that the plan is possible to implement, and all the proposed algorithms can be further reported.
  * No need to implement a full algorithm at this step. For example, if your library is devoted to the feature selection algorithm, just implement a ridge regression, BUT fully compatible with library interface.
	 * **Evaluation criterion:** presentation  at Tech. meeting 2


* Project wrapping:
	* Making the code uniform across all the teammates
	* Controlling the code quality/consistency
	* Wrapping the code into library, repository creation and support
	* **Evaluation criterion:** cross-review,  presentation, the links are correct, the code can be installed without problems, all the workflows are setup, short presentation at Checkpoint, full presentation at tech. meeting 3

  
* Tests writing
	* **Evaluation criterion:** test coverage > 90%,  presentation at Tech. meeting 3
* Documentation writing
	* **Evaluation criterion:** cross-review,   presentation at Tech. meeting 2 (intermediate version), presentation at Tech. meeting 3
* Cross-review (1 activity per teammate)
* Making a final demo based on the basic code
	* **Evaluation criterion:** cross-review,  presentation
  
* Blog post and tech. report
	* Blog post must be published at some platform (habr, medium, etc)
	* Short message: up to 10 minutes
	* **Evaluation criterion:** ,  presentation at Tech. meeting 2 (intermediate version), ,presentation at Tech. meeting 3, possibely external review

 
* Tech. report: must contain a short version of technical paper: abstract, introduction, methods, experiments. The length: 3-5 pages.
	* **Evaluation criterion:** ,  presentation at Tech. meeting 2 (intermediate version), ,presentation at Tech. meeting 3, possibely external review


* Algorithm implementation (1 activity per teammate)
	*  **Evaluation criterion:** presentation at Tech. meeting 1, cross-review, presentation, tests correctly run the algorithm,  presentation at Tech. meeting 3

For a small team (<4) some activites can be reduced.



## Project list, fall 2026
### Secret energy-based models

**Number of people in team:**  2-4

**Motivation**:  the project treats *sampling/generation* as the main lens: nearly-standard architectures trained for other purposes (classification, discrimination, denoising) turn out to be energy-based models (EBM), and the same energy view lets you turn them into generators at very different costs — from a free walk on top of an already-trained network to a fully retrained classifier. 


**Algorithms to implement (from simplets to hardest):**
* [Denoising and contrastive autoencoders as EBM](https://arxiv.org/abs/1211.4246)
* [JEM: Your Classifier is Secretly an Energy Based Model and You Should Treat it Like One](https://arxiv.org/abs/1912.03263)
* [Discriminator as EBM](https://arxiv.org/pdf/2003.06060)
* [JEM++](https://arxiv.org/pdf/2109.09032) and [SADA-JEM](https://arxiv.org/pdf/2209.07959): engeneering tricks for training JEM

**Project specifics:** JEM++ and SADA-JEM are strongly dependent on JEM and can be considered as helpers/utils for trianing JEM. These tasks are very co-related.

**Problem details:**  sample quality, especially for JEM, will likely be mediocre (JEM/SGLD training is notoriously unstable). Regardless of generation quality, the library must expose an out-of-distribution detection utility built on the *same* energy function at (near-)zero extra cost ([Liu et al., Energy-based OOD Detection](https://arxiv.org/abs/2010.03759)) for all three host models. 


### Low-variance gradient estimation for arbitary distributions

**Number of people in team:** 2-3

**Motivation**: The vanilla ELBO estimation in generative models like VAE uses reparametrization trick: a method of sampling random variables with low variance of the gradient of parameter distribution. The problem with this method is that it's available only for the limited number of distributions. The goal of this project is to wrap multiple methods describing a solution for this issue into a library performing for (nearly-)arbitary distributions.
 
**Algorithms to implement (from simplets to hardest):**
* [Rejection-sampling variational inference](https://proceedings.mlr.press/v54/naesseth17a.html)
* [Implicit reparametrization trick: case for factorized distribution]((https://arxiv.org/abs/1805.08498)
* [Transort equation-based reparametrization trick](https://proceedings.mlr.press/v80/jankowiak18a/jankowiak18a.pdf)


**Recommended stack**: one can use pytorch/pyro (both have interfaces for distributions) or distrax for JAX. Other stack can also be used.

**Note:** for the comparison it's recommended to implement REINFORCE-based methods, as well as some numerical low-dimmesnional methods.

**Other links:**
* [Previous project attemp](https://github.com/intsystems/implicit-reparameterization-trick)
* [Discussion of IRP in the TF probability thread](https://github.com/tensorflow/probability/issues/51?ref=https://githubhelp.com)
* [Some more discussions in the pytorch thread](https://discuss.pytorch.org/t/pytorch-reparametrization-method-for-gamma-dirichlet-von-mises-distribution/109472)
* [Mixutre distribution implementation](https://github.com/vsimkus/torch-reparametrised-mixture-distribution) 
* [Lab on the implementation of IRT](https://github.com/intsystems/BMM/blob/main-22/lab2/BarabanshchikovaTask2.ipynb)


###  Low-variance gradient estimation for mixture distributions

**Number of people in team:** 2-4

**Motivation**: Standard reparameterization trick in generative models like VAE works well for basic distributions, but fails for mixture distributions due to discrete component sampling. PyTorch's native `MixtureSameFamily` doesn't support `rsample()` for gradients over mixture parameters. The goal of this project is to build a library implementing continuous, low-variance gradient estimation methods specifically for mixture models.

**Algorithms to implement (from simplest to hardest):**
* [Score-function baseline with Sticking the Landing (STL) trick](https://arxiv.org/abs/1703.09194) ([See also](https://www.jmlr.org/papers/v27/25-2560.html))
* [Stratified mixture estimator (multi-sample)](https://www.jmlr.org/papers/v27/25-2560.html)
* [Implicit reparameterization trick for mixture distributions](https://arxiv.org/abs/1805.08498)
* [Post-stratified mixture estimator (single-sample continuous transport)](https://www.jmlr.org/papers/v27/25-2560.html)

**Recommended stack**: PyTorch (extending `torch.distributions`) or Distrax for JAX.

**Note:** For comparison, methods should be benchmarked on synthetic multimodal targets, Mixture-of-Gaussians VAE, and BNNs with mixture priors (comparing gradient variance vs wall-clock time).

**Other links:**
* [Gradient Estimation for Mixture Variational Inference (JMLR 2026)](https://www.jmlr.org/papers/v27/25-2560.html)
* [Implicit Reparameterization Trick paper](https://arxiv.org/abs/1805.08498)
* [Pathwise Derivatives for Multivariate Distributions paper](https://proceedings.mlr.press/v80/jankowiak18a/jankowiak18a.pdf)
* [Sticking the Landing paper](https://arxiv.org/abs/1703.09194)
* [Previous mixture distribution implementation attempt](https://github.com/vsimkus/torch-reparametrised-mixture-distribution)
* [PyTorch issue on mixture reparameterization](https://github.com/pytorch/pytorch/issues/24249)


### Neural compression for scientific data 

**Number of people in team:**  2-4

**Motivation**:  information theory and Bayesian models are deeply tied. Here we propose to implement multiple variational and neural compression methods for losesless (and nearly-loseless) compression. In spite of well-established compression models, such as [NeuralCompression](https://github.com/facebookresearch/NeuralCompression) focused at generic media, we will focus more on the scientific data, that has a complicated covariance structure.

**Algorithms to implement:**
* [Lossy compression](https://proceedings.neurips.cc/paper/2021/file/7535bbb91c8fde347ad861f293126633-Paper.pdf)
* [Var. inference-based](https://arxiv.org/pdf/1901.04866)
* [Transformer-based](https://openreview.net/forum?id=Hygi7xStvS)
* [Gradient flows-based](https://arxiv.org/pdf/1905.07376)

**Note:** good start is to look at [this](https://github.com/facebookresearch/NeuralCompression), [this repo](https://github.com/fahaihi/NNLCB?tab=readme-ov-file), [torchac](https://github.com/fab-jul/torchac), [craystack](https://github.com/j-towns/craystack)

### Theoretically informed deep learning model complexity estimation

**Number of people in team:**  2-4

**Motivation**: In classical statistics we have multiple standard ways for model selection (AIC, BIC, R^2 and its variations). Most of them are unapplicable for lage deep learning models. In this project we will try to implement different approaches for model complexity estimations and compare them.

**Algorithms to implement:**
* Basic methods: AIC, BIC, HQIC, WAIC, WBIC, [2-part MDL codes](https://arxiv.org/abs/math/0406077)  
* Bayesian-based codes: [Variational coding](https://papers.nips.cc/paper/4329-practical-variational-inference-for-neural-networks) and [KFAC-Laplace-based Evidence](https://openreview.net/challenge?redirect=%2Fforum%3Fid%3DSkdvd2xAZ)
    * Although these methods are Bayesian, we need a bridge between them and MDL in the interface part. See  [Variational coding](https://papers.nips.cc/paper/4329-practical-variational-inference-for-neural-networks) and Section "2.6.3" from [MDL tutorial](https://arxiv.org/abs/math/0406077) 
* [Online coding](https://arxiv.org/abs/2210.07931)
    * The basic approach itself is very easy, you need to implement and compare the prequential coding variants discussed in the paper. (TBD)
* [Compression-based generalization](https://proceedings.mlr.press/v80/arora18b/arora18b.pdf)
