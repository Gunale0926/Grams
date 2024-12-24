# Grams: Gradient Descent with Adaptive Momentum Scaling
[![arXiv](https://img.shields.io/badge/arXiv-2412.17107-b31b1b.svg)](https://arxiv.org/abs/2412.17107) [![PyPI - Version](https://img.shields.io/pypi/v/grams-pytorch)](https://pypi.org/project/grams-pytorch/)

<img width="838" alt="image" src="https://github.com/user-attachments/assets/54f77c6c-54f8-480f-9070-11f0c5060cd0" />

## Install
```bash
pip install grams-pytorch
```

## How to use
Import:
```python
from grams import Grams
```

Instantiate:
```python
optimizer = Grams(lr=1e-3, weight_decay=0.0)
```
