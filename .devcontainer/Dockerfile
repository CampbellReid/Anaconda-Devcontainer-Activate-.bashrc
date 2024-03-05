FROM mcr.microsoft.com/devcontainers/universal:2-linux

RUN apt-get update && apt-get install -y libgl1

COPY .devcontainer/environment.yml /tmp/conda-tmp/
RUN conda env create -f /tmp/conda-tmp/environment.yml

COPY .devcontainer/conda_extra /home/codespace/
RUN cat /home/codespace/conda_extra >> /home/codespace/.bashrc