FROM continuumio/miniconda3
LABEL maintainer='akisatok <akisato@ieee.org>'
LABEL Description='This is an extension of the official miniconda3 docker image. The following packages are additionally installed: numpy, scipy, pandas, matplotlib, scikit-learn, jupyter, jupyterlab, nodejs.'

RUN conda install numpy scipy pandas matplotlib scikit-learn
RUN conda install -c conda-forge jupyter jupyterlab
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs
