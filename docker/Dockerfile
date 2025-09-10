# 使用Ubuntu22.04作为基础镜像
FROM ubuntu:22.04

# 设置非交互模式避免tzdata等包安装卡住
ENV DEBIAN_FRONTEND=noninteractive

# 更新并安装常用开发工具
RUN apt-get update && apt-get install -y \
    # g++ make等基础工具
    build-essential \
    cmake \
    # 比make更快的ninja
    ninja-build \
    git \
    wget \
    curl \
    unzip \
    # 用于发现库
    pkg-config \
    # OpenGL开发库
    libglu1-mesa-dev \
    freeglut3-dev \
    mesa-common-dev \
    libglew-dev \
    libglfw3-dev \
    libglm-dev \
    # Qt6开发库
    qt6-base-dev \
    qt6-base-dev-tools \
    qt6-tools-dev \
    qt6-tools-dev-tools \
    qt6-l10n-tools \
    qt6-declarative-dev \
    qt6-multimedia-dev \
    #qt6-svg-dev \
    # 其他常用工具
    gdb \
    clang \
    vim \
    && rm -rf /var/lib/apt/lists/*

# 设置工作目录
VOLUME /root/env
WORKDIR /root/env

# 默认进入 bash
CMD ["/bin/bash"]