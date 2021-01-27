FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y software-properties-common
RUN add-apt-repository universe
RUN apt-get install -y python libstdc++6 python-setuptools libgconf-2-4 python3-pip
RUN apt-get update -y
RUN pip3 install virtualenv
RUN virtualenv venv
RUN cd venv && . bin/activate && pip install turicreate
#RUN pip3 install --upgrade pip
#RUN pip3 install turicreate





