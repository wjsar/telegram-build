FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Asia/Shanghai
RUN apt-get update && apt-get install -y \
    git \
    cmake \
    build-essential \
    qt5-default \
    libqt5core5a \
    libqt5gui5 \
    libqt5widgets5 \
    libqt5network5 \
    libqt5multimedia5 \
    python3 \
    gyp \
    ninja-build \
    pkg-config \
    libssl-dev \
    zlib1g-dev \
    libxcb1-dev \
    libxcb-keysyms1-dev \
    libxcb-icccm4-dev \
    libxcb-image0-dev \
    libxcb-shm0-dev \
    libxcb-xfixes0-dev \
    libxcb-render0-dev \
    libxcb-util0-dev \
    libxcb-randr0-dev \
    libasound2-dev \
    libpulse-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /telegram
COPY . .

RUN mkdir -p build
RUN cd build && \
    cmake -GNinja -DCMAKE_BUILD_TYPE=Release ..

CMD ["ninja", "-C", "build"] 