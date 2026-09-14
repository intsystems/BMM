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
