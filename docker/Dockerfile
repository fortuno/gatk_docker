FROM fedora:24

MAINTAINER Jeremiah H. Savage <jeremiahsavage@gmail.com>

RUN dnf install -y \
       java-1.8.0-openjdk-headless \
       maven \
       tar \
       wget \
    && wget https://github.com/broadgsa/gatk-protected/archive/3.6.tar.gz \
    && tar xf 3.6.tar.gz \
    && cd gatk-protected-3.6 \
    && bash ./ant-bridge.sh \
    && mv target/GenomeAnalysisTK.jar /usr/local/bin/ \
    && cd ../ \
    && rm -rf gatk-protected-3.6 \
    && cd
