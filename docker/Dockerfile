
##### CHOOSE YOUR UBUNTU...

# For python 3.8 use 20.4
#FROM ubuntu:20.04

# For python 3.6 use 18.04
from ubuntu:18.04

## Building the image
## ------------------
## docker build --tag turicreate .
## Running
## -------
## docker run -it --name turicreate turicreate

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y software-properties-common
RUN add-apt-repository universe
RUN apt-get install -y python libstdc++6 python-setuptools libgconf-2-4 python3-pip iproute2 wget unzip
RUN apt-get update -y
RUN pip3 install virtualenv
RUN virtualenv venv
RUN cd /venv && . bin/activate && pip3 install --upgrade pip
RUN cd /venv && . bin/activate && pip install turicreate==6.4.1
COPY samples /venv/samples

RUN cd /venv/samples/image-clasification/ && wget -nv https://download.microsoft.com/download/3/E/1/3E1C3F21-ECDB-4869-8368-6DEBA77B919F/kagglecatsanddogs_3367a.zip
RUN cd /venv/samples/image-clasification/ && unzip kagglecatsanddogs_3367a.zip
CMD cd /venv && . bin/activate && bash





