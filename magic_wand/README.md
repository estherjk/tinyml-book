# magic_wand

## Arduino Project Setup

Copy and paste `ARDUINO_LSM9DS1` into your local Arduino libraries folder (e.g. `~/Documents/Arduino/libraries`)

## Notebook Setup (with Docker)

### Build

```bash
docker build -t tinyml_magic_wand:latest .
```

### Run

```bash
docker run --gpus all \
    -it --rm \
    -p 8888:8888 \
    -p 6006:6006 \
    -v $PWD/notebook:/tf/notebooks \
    tinyml_magic_wand:latest
```