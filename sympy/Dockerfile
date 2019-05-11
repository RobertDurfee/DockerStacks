FROM ubuntu:18.04

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip

RUN pip3 install \
    jupyter \
    sympy

RUN useradd -ms /bin/bash usympy
USER usympy

WORKDIR /home/usympy/work