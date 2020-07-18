# micro_speech

## Notebook Setup (with Docker)

### Build

```bash
docker build -t tinyml_micro_speech:latest .
```

### Run

```bash
docker run --gpus all \
    -it --rm \
    -p 8888:8888 \
    -p 6006:6006 \
    -v $PWD/notebook:/tf/notebooks \
    tinyml_micro_speech:latest
```