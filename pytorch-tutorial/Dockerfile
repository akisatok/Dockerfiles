FROM akisatok/pytorch-base
LABEL maintainer='akisatok <akisato@ieee.org>'
LABEL Description='Specialized for my pytorch tutorial shown in github.'

# labextentions in jupyter
## jupyterlab-manager
RUN conda install -qyc conda-forge ipywidgets
## tensorboard
RUN conda install --qyc conda-forge tensorflow
RUN pip install -q --no-cache-dir jupyter-tensorboard
## kite
RUN wget -q -O /tmp/kite-setup.sh https://linux.kite.com/dls/linux/current
RUN chmod +x /tmp/kite-setup.sh
RUN /tmp/kite-setup.sh --download /tmp/kite-installer
RUN /tmp/kite-installer install
RUN rm -f /tmp/kite-setup.sh /tmp/kite-installer
RUN pip install -q --no-cache-dir jupyter-kite
## install
RUN jupyter labextension install @jupyterlab/toc @jupyter-widgets/jupyterlab-manager jupyterlab-emacskeys jupyterlab_tensorboard @kiteco/jupyterlab-kite
