FROM nvidia/cuda:10.2-cudnn8-devel-ubuntu18.04
LABEL maintainer='akisatok <akisato@ieee.org>'
LABEL Description='An extension of the official NVIDIA CUDA Docker image for the use of pytorch.'

# curl
RUN apt-get update -qq
RUN apt-get install -qq -y curl

# miniconda
WORKDIR /opt
RUN bash -c 'curl -sL https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o miniconda.sh'
RUN chmod +x miniconda.sh
RUN /opt/miniconda.sh -bup /opt/miniconda3
RUN rm -f miniconda.sh
ENV PATH /opt/miniconda3/bin:$PATH
RUN . /opt/miniconda3/etc/profile.d/conda.sh

# fundamental data science tools
RUN conda install --quiet --yes numpy scipy pandas matplotlib scikit-learn
RUN conda install --quiet --yes -c conda-forge jupyter jupyterlab

# node.js
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -qq -y nodejs
RUN conda install --quiet --yes nodejs

# pytorch
RUN conda install -qyc pytorch pytorch torchvision
