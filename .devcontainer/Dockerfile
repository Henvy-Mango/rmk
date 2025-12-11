FROM rust:latest

ENV SHELL /bin/bash

RUN apt-get update && apt-get install -y \
    bash-completion \
    libclang-dev \
    usbutils \
    git \
    curl

RUN apt-get clean -y && \
  apt-get autoremove --purge -y && \
  rm -rf /var/lib/apt/lists/*

RUN mkdir -p /root/.vscode-server/extensions

# Set working directory
WORKDIR /workspace
VOLUME ["/workspace"]

CMD ["/bin/bash"]