# This dockerfile is for Tommy's debian
# VERSION 1.0.0
# Author: Tommy
# Command format: Instruction [arguments / command] ..

# Base image to use
FROM debian:buster

# Maintainer:
MAINTAINER Tommy ab9986@qq.com

# Commands to update the image
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak
RUN echo  "deb http://mirrors.cloud.tencent.com/debian buster main contrib non-free"  >>/etc/apt/sources.list
RUN echo  "deb http://mirrors.cloud.tencent.com/debian buster-updates main contrib non-free" >>/etc/apt/sources.list
RUN echo  "deb-src http://mirrors.cloud.tencent.com/debian buster main contrib non-free" >>/etc/apt/sources.list
RUN echo  "deb-src http://mirrors.cloud.tencent.com/debian buster-updates main contrib non-free" >>/etc/apt/sources.list
RUN apt-get clean all
RUN apt-get update
RUN apt-get upgrade -y  
# Install 
RUN apt-get install -y vim emacs git

# New group ab9986 and New user tommy
RUN groupadd -r ab9986 && useradd -r -m -g ab9986 tommy
# tommy run docker
USER tommy
WORKDIR /home/tommy
RUN whoami
RUN pwd


# do some thing
RUN git config --global http.sslverify false
RUN cd /home/tommy/
RUN rm -rf .emacs.d
ENV TERM xterm-256color
ENV LANG=zh_CN.UTF-8




