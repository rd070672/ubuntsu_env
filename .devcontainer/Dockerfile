# ベースとなる Ubuntu
FROM ubuntu:22.04

# apt の質問をなくすおまじない
ENV DEBIAN_FRONTEND=noninteractive

# Ubuntu の基本パッケージと Python をインストール
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    curl \
    wget \
    vim \
    python3 \
    python3-pip \
    python3-venv \
    && rm -rf /var/lib/apt/lists/*

# よく使う Python ライブラリをあらかじめ入れておく
RUN pip3 install --no-cache-dir \
    numpy \
    scipy \
    matplotlib \
    pandas \
    jupyterlab