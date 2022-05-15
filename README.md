# 9143-HPML-Project

- Project title: Voice Separation and Optimization in Recurrent Neural Networks
- Team members: Leo Hu, Junda Ai

## Introduction

In this project we looked into two state-of-the-art voice separation model implementations, and anaylzed the effects of different optimization algorithms and techniques on them.

### SVoice

[SVoice: Speaker Voice Separation using Neural Nets](https://github.com/facebookresearch/svoice)

- [Hydra](https://hydra.cc/) to manage training configurations
- Custom implementation of [SI-SNR](https://arxiv.org/abs/1711.00541) loss function
- Adam optimizer
- Gradient clipping

## Getting started

[SVoice experiment](https://colab.research.google.com/drive/1B1cNeMLSL0KVs-Am1dKA5_F4E6k474_d#scrollTo=9DPpT3KiFTn2) was carried out on Google Colab.

Jupyter notebooks for ploting validation results:

- [svoice_grad_clip](svoice_grad_clip.ipynb)
- [svoice_lr_schl](svoice_lr_schl.ipynb)
- [svoice_optim](svoice_optim.ipynb)

## Experiment results

### SVoice

- Adam yields the best results among gradient descent optimizers
- Plateau learning rate (decay when a metric stops improving) scheduler with Adam works better than StepLR (step-wise decay)
- Gradient clipping further improves performance

Gradient descent optimizers:

![Optimizers](img/svoice-optim.png)

LR schedulers:

![LR schedulers](img/svoice-lr-schl.png)

Gradient clipping:

![Gradient clipping](img/svoice-gradient-clipping.png)
