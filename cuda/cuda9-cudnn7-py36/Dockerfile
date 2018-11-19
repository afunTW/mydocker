FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04
LABEL maintainer=afun@afun.tw
SHELL ["/bin/bash", "-c"] 
WORKDIR /root

# Install pyenv
RUN apt-get update && apt-get install -y git vim curl
RUN curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
RUN echo 'export PATH="/root/.pyenv/bin:$PATH"' >> ~/.bashrc
ENV PATH="/root/.pyenv/bin":"/root/.pyenv/versions/3.6.5/bin":$PATH
RUN eval "$(pyenv init -)" && \
    eval "$(pyenv virtualenv-init -)"

# Install python 3.6.5 by pyenv
RUN apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
    xz-utils tk-dev
RUN pyenv install 3.6.5
