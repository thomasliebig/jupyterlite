FROM docker.io/manimcommunity/manim:v0.18.0

COPY --chown=manimuser:manimuser . /manim

RUN mkdir -p ~/miniconda3
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
RUN bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
RUN rm -rf ~/miniconda3/miniconda.sh
RUN ~/miniconda3/bin/conda init bash

RUN conda install python=3.7
RUN conda install rise
RUN conda install cython
RUN conda install ipython
RUN conda install ipywidgets
RUN conda install numpy
RUN conda install matplotlib
RUN conda install pandas
RUN conda install scikit-image
RUN conda install scikit-learn
RUN conda install sympy
RUN conda install bokeh

RUN pip install jupyter-contrib-nbextensions
RUN pip install notebook==6.1.5

RUN jupyter contrib nbextension install --user
RUN jupyter nbextension enable splitcell/splitcell
RUN jupyter nbextension enable python-markdown/main







