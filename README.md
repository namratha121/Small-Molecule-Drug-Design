# Small-Molecule-Drug-Design

Conventional drug design is expensive and slow, taking over a decade and billions of dollars per drug. In this project, we explore AI-driven de novo drug design using a deep learning model, Generative Adversarial Network (GAN). We specifically implement a GAN to generate valid molecular structures that can be potential drug candidates. The model is trained on the QM9 Dataset and leverages GAN to generate drug like molecules with optimized properties such as validity, uniqueness, novelty etc.

Dataset : 
QM9 Dataset : Contains 134k small organic molecules with up to 9 heavy atoms (C,O,N,F)

Files : 
1. main_gan.py - Main training script for GAN Model
2. models_gan.py - This file defines the Generator and Discriminator neural networks used in the GAN architecture for graph-structured data.
3. data_loader.py - Handles loading and preprocessing of the QM9 dataset
4. utils.py - This file provides a comprehensive suite of molecular evaluation metrics for assessing the quality of generated molecules.
5. layers.py - This file defines the building blocks used to construct the Generator and Discriminator models, specifically designed for graph-based data.
6. args.py - This module configures training and testing parameters for GAN

Metrics : 

Validity : % of generated molecules that are chemically valid

Novelty : % of valid molecules not in training data

Uniqueness : % of non duplicate valid molecules

Natural Product Score: Estimates how "natural product-like" a molecule is, using a pretrained model.

QED (Drug-likeness): Quantitative Estimation of Drug-likeness score.

LogP: Measures water-octanol partition coefficient (a common drug property).

SA Score: Synthetic Accessibility, indicating how easy a molecule is to synthesize.

Diversity: Measures structural diversity compared to a reference set.

