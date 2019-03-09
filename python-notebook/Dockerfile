# Start with the latest ubuntu image
FROM ubuntu:18.04

# Install Python 3
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip

# Install Jupyter
RUN pip3 install jupyter

# Set up the user
RUN useradd -ms /bin/bash jovyan
USER jovyan

# Set working directory in container
WORKDIR /home/jovyan/work

# Launch the jupyter notebook
ENTRYPOINT [ "jupyter", "notebook", "--ip=0.0.0.0" ]