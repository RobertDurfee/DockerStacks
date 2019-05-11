# Start with the latest ubuntu image
FROM ubuntu:18.04

# Install packages
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    openjdk-11-jdk \
    unzip

# Install Jupyter
RUN pip3 install jupyter

# Add the IJava kernel
COPY ijava-1.2.0.zip /tmp/
RUN unzip /tmp/ijava-1.2.0.zip -d /tmp/ijava-1.2.0/
RUN rm /tmp/ijava-1.2.0.zip
RUN cd /tmp/ijava-1.2.0 && python3 ./install.py --sys-prefix
RUN rm -r /tmp/ijava-1.2.0

# Set up the user
RUN useradd -ms /bin/bash ujava
USER ujava

# Set working directory in container
WORKDIR /home/ujava/work