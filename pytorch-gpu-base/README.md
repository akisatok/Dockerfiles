# pytoch-gpu-base

An extension of the official NVIDIA CUDA Docker image for the use of pytorch.

## Base

[nvidia/cuda:10.2-cudnn8-devel-ubuntu18.04](https://hub.docker.com/r/nvidia/cuda/tags?page=1&name=10.2-cudnn8-devel-ubuntu)

## Additional packages

* conda install
  * numpy, scipy, pandas, matplotlib, scikit-learn
  * conda-forge: jupyter, jupyterlab
  * pytorch: pytorch, torchvision
  * nodejs (for jupyterlab labextension)
* apt-get install
  * nodejs (for jupyterlab labextension)

## Commands

```
$ docker pull akisatok/pytorch-gpu-base
$ docker run -it -p 8888:8888 -v /home/hoge:/home/hoge --name pytorch-base akisatok/pytorch-gpu-base
```
