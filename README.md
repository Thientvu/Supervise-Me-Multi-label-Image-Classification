# Supervise Me: Multi-label Image Classification

## Overview

This project addresses the health risks astronauts face from ionizing radiation during spaceflight. We focus on predicting DNA damage in cells using the BPS Mice Microscopy Dataset. Our machine learning models analyze fluorescent cell images, classifying them by particle type or both particle type and dosage.

## Challenge

Astronauts encounter health hazards such as DNA damage, central nervous system effects, and immune system effects due to ionizing radiation. Galactic cosmic rays, a significant source, create DNA damage visible through fluorescent imaging.

## Data

The BPS Mice Microscopy Dataset from NASA GeneLab provides images of radiated mice cells. The dataset includes particle type, dosage, and imaging times post-exposure.

## Methodology

We used Convolutional Neural Networks (CNNs), specifically LeNet-5, for image classification. We compared results with a baseline MLPClassifier. Data preprocessing included normalization, resizing, and augmentation.

## Project Pipeline

Our design sprint involved collaboration, mapping the process, and setting safe, stretch, and bold goals. We consulted domain experts, identified obstacles, and proposed end-to-end solutions.

## Replicability

The GitHub repository ensures replicability. Data retrieval scripts, model training scripts, and hyperparameter configurations are organized. Weights and Biases were used for logging experiments.

## Results

The LeNet Image Classifier outperformed the baseline MLPClassifier. Single-label predictions had higher validation accuracy than multi-label predictions.

## Future Work

Future steps include enhancing the deep learning model complexity, exploring advanced CNN architectures, and developing an API for real-time predictions and dataset contribution.

## Repository Structure

- `data`: Contains space for cell images.
- `src`: Scripts for downloading data and running machine learning models.
- `environment/setup`: Yaml files for software installation.

## How to Replicate

1. Execute `src/dataset/bps_datamodule.py` to download training images.
2. Configure hyperparameters in `src/models/lenet_scratch.py` and `mlp_model.py`.
3. Execute the respective model files.

## References

- [Quickstart Guide to Weights and Biases Sweeps](https://docs.wandb.ai/guides/sweeps/quickstart)
- [Multi-Label Image Classification with PyTorch and Deep Learning](https://debuggercafe.com/multi-label-image-classification-with-pytorch-and-deep-learning/)
- [Biological and Physical Sciences (BPS) Microscopy Benchmark Training Dataset](https://registry.opendata.aws/bps_microscopy)

## Acknowledgements

Special thanks to collaborators Lauren Sanders, Ph.D., Sylvain Costes, Ph.D., and Kevin Li for dataset provision, domain expertise, and insights on transfer learning. Adapted from materials in The Frontier Development Lab summer research program.