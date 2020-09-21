FROM akisatok/miniconda3-base
LABEL maintainer='akisatok <akisato@ieee.org>'
LABEL Description='This is an extension of the official miniconda3 docker image. The following packages are additionally installed: numpy, scipy, pandas, matplotlib, scikit-learn, jupyter, jupyterlab, nodejs.'

# pytorch
RUN conda install -c pytorch pytorch torchvision
