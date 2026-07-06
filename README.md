# Reproducing AOT-GAN for High-Resolution Image Inpainting

> Reproduction of **AOT-GAN: Aggregated Contextual Transformations for High-Resolution Image Inpainting** using the official implementation.

![Python](https://img.shields.io/badge/Python-3.8-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-1.8.1-red)
![License](https://img.shields.io/badge/License-Apache%202.0-green)


## Project Overview

This repository documents my successful reproduction of the **AOT-GAN** model for high-resolution image inpainting.

The objective of this project was to understand the complete training pipeline of a state-of-the-art GAN-based image inpainting model, train it using the official implementation, and reproduce the qualitative results reported in the research paper.

This project helped me gain practical experience in:

- Deep Learning
- Generative Adversarial Networks (GANs)
- Image Inpainting
- PyTorch
- Model Training
- Performance Evaluation
- Research Paper Reproduction

---

## Project Highlights

- Successfully reproduced the AOT-GAN image inpainting model.
- Trained the model using the official implementation.
- Generated high-quality image inpainting results.
- Evaluated the trained model using standard image quality metrics.
- Studied the architecture and complete training pipeline of AOT-GAN.

---

## Original Paper

**AOT-GAN: Aggregated Contextual Transformations for High-Resolution Image Inpainting**

**Authors**

- Yanhong Zeng
- Jianlong Fu
- Hongyang Chao
- Baining Guo

Paper:
https://arxiv.org/abs/2104.01431

Official Repository:
https://github.com/researchmm/AOT-GAN-for-Inpainting

---

# My Contribution

This repository represents my reproduction of the original AOT-GAN implementation.
The primary goal of this project was to understand the implementation details, successfully train the model, and verify the published results using the official source code.

During this project I:

- Configured the complete training environment.
- Installed all required dependencies.
- Prepared the required datasets and masks.
- Successfully trained the AOT-GAN model.
- Generated inpainting results using the trained model.
- Evaluated the generated outputs using the provided evaluation scripts.
- Studied the complete architecture and training workflow.
- Reproduced the qualitative image inpainting results reported in the paper.

---

# Model Architecture

AOT-GAN introduces two major improvements for high-resolution image inpainting.

### Aggregated Contextual Transformations (AOT Block)

The generator employs Aggregated Contextual Transformation (AOT) Blocks that aggregate contextual information using multiple receptive fields.

This enables the network to better infer missing semantic content while preserving structural consistency.

### SoftGAN Discriminator

The discriminator incorporates an auxiliary mask prediction task that improves texture synthesis and encourages the generator to produce realistic image details.

---

# Repository Structure

```
AOT-GAN-Image-Inpainting-Reproduction/

│── experiments/
│── src/
│── environment.yml
│── LICENSE
│── README.md
```

---

# Requirements

- Python 3.8.8
- PyTorch 1.8.1
- CUDA-enabled GPU (recommended)
- Conda

---

# Installation

Clone the repository

```bash
git clone https://github.com/psmlikhitha/AOT-GAN-Image-Inpainting-Reproduction.git

cd AOT-GAN-Image-Inpainting-Reproduction
```

Create the environment

```bash
conda env create -f environment.yml

conda activate inpainting
```

---

# Dataset Preparation

Download the required training images and masks.

Specify the dataset paths using

```
--dir_image
--dir_mask
```

---

# Training

Train the model

```bash
cd src

python train.py
```

Resume training

```bash
python train.py --resume
```

---

# Testing

Run inference

```bash
cd src

python test.py --pre_train <checkpoint_path>
```

---

# Evaluation

Evaluate generated images

```bash
python eval.py \
--real_dir <ground_truth> \
--fake_dir <generated_results> \
--metric mae psnr ssim fid
```

Supported metrics

- MAE
- PSNR
- SSIM
- FID

---

## Results

The model was successfully trained using the official implementation.

The generated outputs demonstrate high-quality image completion that is consistent with the qualitative results reported in the original AOT-GAN paper.

Sample output images, training logs, and qualitative comparisons will be added in a future update.


---

# Skills Demonstrated

- Python
- PyTorch
- Computer Vision
- Deep Learning
- GANs
- Image Inpainting
- Model Training
- Performance Evaluation
- Linux
- Research Reproduction

---

# Learning Outcomes

Through this project, I gained practical experience in:

- Understanding GAN-based image inpainting architectures.
- Preparing datasets for large-scale model training.
- Training and evaluating deep learning models.
- Managing experiment configurations.
- Reproducing results from published research.

---

## Future Work

- Add qualitative comparison images between the original and reproduced results.
- Include sample outputs generated by the trained model.
- Document the complete training configuration and hyperparameters.
- Explore fine-tuning on additional image datasets.

---

# Acknowledgements

This repository is a reproduction of the original **AOT-GAN** implementation.

The original architecture, research paper, and source code were developed by the original authors.

Full credit for the algorithm and implementation belongs to them.

If you use this work for research, please cite the original paper.

---

# Citation

```bibtex
@inproceedings{yan2021agg,
  author = {Zeng, Yanhong and Fu, Jianlong and Chao, Hongyang and Guo, Baining},
  title = {Aggregated Contextual Transformations for High-Resolution Image Inpainting},
  booktitle = {Arxiv},
  year = {2020}
}
```

---

# License

This repository follows the Apache 2.0 License of the original implementation.