FROM ubuntu:24.04

# evitar interação com o usuário durante a instalação de pacotes
ENV DEBIAN_FRONTEND=noninteractive

# dependências básicas
RUN apt-get update && apt-get install -y \
    curl \
    git \
    python3 \
    python3-pip \
    build-essential \
    gcc \
    g++ \
    make \
    sox \
    gstreamer1.0-tools \
    gstreamer1.0-plugins-good \
    gstreamer1.0-plugins-base \
    gstreamer1.0-plugins-base-apps \
    ca-certificates \
    gnupg

# node.js
RUN curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs

# Edge Impulse
RUN npm install -g edge-impulse-linux --unsafe-perm

CMD ["/bin/bash"]
