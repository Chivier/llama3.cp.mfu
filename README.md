# llama3.np

`llama3.cp` is an adapted version of `llama3.np` (pure NumPy) that utilizes CuPy for GPU acceleration. The original implementation, written in pure NumPy, was created by [likejazz](https://github.com/likejazz/llama3.np).

## Usage

```shell
python llama3_gpu.py "I have a dream"
"""
I have a dream. He dream of a big, beautiful garden full of flower and tree. He dream of playing with hi friend and eating yummy snack.
One day, he wa walking in the garden when he saw

Token count: 50, elapsed: 0.89s, 56 tokens/s
"""
```

On my machine, the original implementation performed as follows:

```shell
python llama3.py "I have a dream"
"""
I have a dream. He dream of a big, beautiful garden full of flower and tree. He dream of playing with hi friend and eating yummy snack.
One day, he wa walking in the garden when he saw

Token count: 50, elapsed: 2.08s, 24 tokens/s
"""
```

## Relevant aspects

Changing from NumPy to CuPy, the performance is improved more than 2 times. Despite this fact, the performance can vary depending on the Hardware.

## Installation

```shell
pip install -r requirements.txt
```

### Observations

Depending on your CUDA version, you must modify the requirements.txt file to install the appropriate version of CuPy. For instance, if you use CUDA 11, you should change the line `cupy-cuda12x` to `cupy-cuda11x`.

## License

MIT
