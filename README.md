# cliscripts

`cliscripts` is a Python library which makes physics simulator for browser easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `cliscripts`, clone and install requirements:

```
git clone https://github.com/user/cliscripts
cd cliscripts
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model procedures --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - background.jpg

```python
from cliscripts import models

model = models.background.jpg(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| procedures | **78.61** | [Code](#), [Paper](#) |
| background.jpg | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

