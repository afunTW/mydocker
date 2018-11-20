FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04
LABEL maintainer=afun@afun.tw
SHELL ["/bin/bash", "-c"] 
WORKDIR /root

# install linux tool and framework
RUN apt-get update
RUN apt-get install -y git vim curl unzip \
    python3.5 python3-pip python2.7 python-pip
RUN pip3 install tensorflow-gpu==1.11.0 keras==2.2.4
RUN pip install tensorflow-gpu==1.11.0 keras==2.2.4