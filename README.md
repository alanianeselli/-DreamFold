# DreamFold
**DreamFold: Generative World Models to dream protein folding pathways in the latent space**

From limited data, World Models can build a latent, approximated representation of the spatiotemporal environment that can be used to train downstream AI models, overcoming data limitation issues. 
We developed DreamFold: a World Model-based generative framework to perform biomolecular simulations. The framework uses variational autoencoders to encode the protein structures and the dihedral moves into latent vectors. We train a feedforward neural network to predict the next latent structure after a latent move, allowing the model to develop its own understanding of the structural dynamics. Finally, in this “hallucinated” latent environment the framework trains an agent with evolutionary algorithms to learn a policy to drive folding simulations towards a target structure. Within the simulations, latent configurations can be decoded back into atomistic structures, allowing the model to be further regularized with Ramachandran-based constraints. Our framework can compute protein folding pathways four orders of magnitude faster (up to ~30000x) than standard MD.

This repository includes the code for the training and inference TrpCage folding trajectories. The model weights for VAE1, VAE2, FFN and Controller are present in the folder files_and_models/ together with the training data stored as .npy files. The raw training data are not included in this repository. So, if you want to run the training yourself, skip step 1 (the rollout data generation step) and start from step2.

<img width="2096" height="1404" alt="fig_for_github" src="https://github.com/user-attachments/assets/b2d720a2-4f41-4806-b306-738f2c4200ff" />

**Contact**
alan.ianeselli@yale.edu

**Reference**
https://www.biorxiv.org/content/10.1101/2025.03.26.645554v1
