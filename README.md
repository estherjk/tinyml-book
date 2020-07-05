# tinyml-book

Development environment & modified samples from the [TinyML Book](https://tinymlbook.com/).

## Project Structure

```bash
.
├── arduino     # Arduino sketches
└── notebooks   # Jupyter notebooks for training & building ML models
```

## Arduino

The device used for this project is the [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense).

## Notebooks

### Host Requirements

* Linux (tested on Ubuntu 20.04)
* NVIDIA GPU

### Docker Usage

#### Build

```bash
docker build -t tinyml-tf:latest .
```

#### Run

```bash
docker run --gpus all \
    -it --rm \
    -p 8888:8888 \
    -p 6006:6006 \
    -v $PWD/notebooks:/tf/notebooks \
    tinyml-tf:latest
```