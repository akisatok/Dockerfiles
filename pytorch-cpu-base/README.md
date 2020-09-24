# pytoch-cpu-base

An extension of the official miniconda3 Docker image for the use of pytorch.

## Base

[continuumio/miniconda3](https://hub.docker.com/r/continuumio/anaconda3/)

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
$ docker pull akisatok/pytorch-base
$ docker run -it -p 8888:8888 -v /home/hoge:/home/hoge --name pytorch-base akisatok/pytorch-base
```
