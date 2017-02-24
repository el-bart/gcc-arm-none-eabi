FROM debian:testing
RUN apt-get update
RUN apt-get install -y vim
RUN apt-get install -y cmake make ninja-build
RUN apt-get install -y wget tar bzip2

RUN cd /opt && \
    wget -O - "https://developer.arm.com/-/media/Files/downloads/gnu-rm/6-2017q1/gcc-arm-none-eabi-6-2017-q1-update-linux.tar.bz2" | tar xjf -
RUN cd /opt && ln -s gcc-arm-none-eabi-6-2017-q1-update gcc-arm-none-eabi

COPY env.cfg /etc/
RUN echo "source /etc/env.cfg" >> /etc/bash.bashrc && echo "source /etc/env.cfg" >> /etc/profile
