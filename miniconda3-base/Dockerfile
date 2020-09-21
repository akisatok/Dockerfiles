FROM continuumio/miniconda3
LABEL maintainer='akisatok <akisato@ieee.org>'
LABEL Description='This is an extension of the official miniconda3 docker image. The following packages are additionally installed: numpy, scipy, pandas, matplotlib, scikit-learn, jupyter, jupyterlab, nodejs.'

RUN conda install --quiet --yes numpy scipy pandas matplotlib scikit-learn
RUN conda install --quiet --yes -c conda-forge jupyter jupyterlab
RUN apt-get update -qq
RUN apt-get install -qq -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -qq -y nodejs
RUN conda install --quiet --yes nodejs
