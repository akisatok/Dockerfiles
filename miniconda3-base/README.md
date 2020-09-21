# miniconda3-base

An extension of the official miniconda3 Docker image. Several packages are additionally installed.

## Base

[continuumio/miniconda3](https://hub.docker.com/r/continuumio/anaconda3/)

## Additional packages

* conda install
  * numpy, scipy, pandas, matplotlib, scikit-learn
  * conda-forge: jupyter, jupyterlab
  * nodejs (for jupyterlab labextension)
* apt-get install
  * nodejs (for jupyterlab labextension)

## Commands

```
$ docker pull akisatok/miniconda3-base
$ docker run -it -p 8888:8888 -v /home/hoge:/home/hoge --name miniconda3-base akisatok/miniconda3-base
```
