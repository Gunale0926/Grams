# Grams: Gradient Descent with Adaptive Momentum Scaling
[![arXiv](https://img.shields.io/badge/arXiv-2412.17107-b31b1b.svg)](https://arxiv.org/abs/2412.17107) [![PyPI - Version](https://img.shields.io/pypi/v/grams-pytorch)](https://pypi.org/project/grams-pytorch/)

Authors: [Yang Cao](https://scholar.google.com/citations?user=pCrKkUQAAAAJ), [Xiaoyu Li](https://scholar.google.com/citations?hl=en&user=WgiSk4AAAAAJ), [Zhao Song](https://scholar.google.com/citations?user=yDZct7UAAAAJ)

This repository contains the official PyTorch implementation for Grams optimizer.

We introduce Gradient Descent with Adaptive Momentum Scaling (Grams), a novel optimization algorithm that decouples the direction and magnitude of parameter updates in deep learning. Unlike traditional optimizers that directly integrate momentum into updates, Grams separates the update direction, derived from current gradients, from momentum, which is used solely for adaptive magnitude scaling. This approach enables Grams to achieve improved loss descent compared to state-of-the-art cautious and momentum-based optimizers.

<img width="838" alt="image" src="https://github.com/user-attachments/assets/54f77c6c-54f8-480f-9070-11f0c5060cd0" />

## Install

Use the following command to install our pytorch implementation for Grams:
```bash
pip install grams-pytorch
```

## How to use Grams

Switching from Adam/AdamW to Grams is simple and requires only two lines of code:

Before:
```python
import torch
optimizer = torch.optim.adam((model.parameters(), lr=1e-3, weight_decay=0.0)
```

Switching to Grams:
```python
from grams import Grams
optimizer = Grams(model.parameters(), lr=1e-3, weight_decay=0.0)
```
Just import Grams and swap the optimizer—everything else remains the same!

## Citation

Please cite our work!
```bibtex
@article{cao2024grams,
  title={Grams: Gradient Descent with Adaptive Momentum Scaling},
  author={Cao, Yang and Li, Xiaoyu and Song, Zhao},
  journal={arXiv preprint arXiv:2412.17107},
  year={2024}
}
```
