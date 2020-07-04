# tinyml-book

Development environment & modified samples from the [TinyML Book](https://tinymlbook.com/).

## Host Requirements

* Linux (tested on Ubuntu 20.04)
* NVIDIA GPU

## Docker Usage

### Build

```bash
docker build -t tinyml-tf:latest .
```

### Run

```bash
docker run --gpus all \
    -it --rm \
    -p 8888:8888 \
    -p 6006:6006 \
    -v $PWD/notebooks:/tf/notebooks \
    tinyml-tf:latest
```