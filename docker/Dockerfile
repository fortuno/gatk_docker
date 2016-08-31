FROM ubuntu:xenial-20160809

MAINTAINER Jeremiah H. Savage <jeremiahsavage@gmail.com>

RUN apt-get update \
    && apt-get install -y \
       openjdk-8-jre-headless \
       maven \
       wget \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && wget https://github.com/broadgsa/gatk-protected/archive/3.6.tar.gz \
    && tar xf 3.6.tar.gz \
    && cd gatk-protected-3.6 \
    && sh ./ant-bridge.sh \
    && mv target/GenomeAnalysisTK.jar /usr/local/bin/ \
    && cd ../ \
    && rm -rf gatk-protected-3.6 \
    && cd
