FROM mcr.microsoft.com/devcontainers/python:2-3.14-trixie

# Install additional OS packages if needed
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive
RUN apt-get -y install --no-install-recommends graphviz


USER vscode

# Install Python dependencies
COPY requirements.txt /tmp/pip-tmp/
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt

RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cpu

# [Optional] Uncomment to install additional packages
# RUN pip3 --disable-pip-version-check --no-cache-dir install <your-package-list-here>
