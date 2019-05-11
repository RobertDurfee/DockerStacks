FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    texlive-full

RUN useradd -ms /bin/bash ulatex
USER ulatex

WORKDIR /home/ulatex/work

ENTRYPOINT [ "pdflatex" ]
