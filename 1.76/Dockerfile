FROM ubuntu:12.04
ENV DEBIAN_FRONTEND=noninteractive
RUN sed -i 's|http://archive.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list && \
  sed -i 's|http://security.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
  cmake \
  git \
  ninja-build \
  ruby \
  gperf \
  bison \
  flex \
  gcc \
  g++ \
  libicu-dev \
  libglib2.0-dev \
  curl \
  gdb \
  python2.7 \
  gettext \
  libcairo-dev \
  fontconfig \
  qt4-qmake qt4-dev-tools \
  make \
  && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/longld/peda.git ~/peda --depth 1
RUN echo "source ~/peda/peda.py" >> ~/.gdbinit
