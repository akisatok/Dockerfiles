# pytoch-tutorial-cpu

Specialized for my pytorch tutorial, which will be presented in github in near future

## Base

[continuumio/miniconda3](https://hub.docker.com/r/continuumio/anaconda3/)

## Additional packages

* conda install
  * numpy, scipy, pandas, matplotlib, scikit-learn
  * conda-forge: jupyter, jupyterlab
  * pytorch: pytorch, torchvision
  * nodejs (for jupyterlab labextension)
  * conda-forge: ipywidgets, tensorflow (for jupyterlab TensorBoard extension)
  * conda-forge: optuna
  * plotly (for optuna visualization)
* pip install
  * jupyterlab-tensorboard, jupyter-kite
  * ray[tune]
* apt-get install
  * nodejs (for jupyterlab labextension)
* Original setup
  * kite
* jupyter labextension install
  * @jupyterlab/toc :  creating Table of Content (ToC) automatically
  * @jupyter-widgets/jupyterlab-manager :  extension manager in jupyter lab/notebook
  * jupyterlab-emacskeys :  Emacs key bind in notebooks
  * jupyterlab_tensorboard :  enabling TensorBoard launch in jupyter lab/notebook
  * @kiteco/jupyterlab-kite :  automatic completion powered by kite

## Commands

(Host)
```
$ docker pull akisatok/pytorch-tutorial
$ docker run -it -p 8888:8888 -v /home/hoge:/home/hoge --name pytorch-tutorial akisatok/pytorch-tutorial
```

(Container)
```
% jupyter lab --allow-root --ip 0.0.0.0
```
