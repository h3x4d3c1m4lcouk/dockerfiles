# See https://hub.docker.com/r/library/python/ for all supported Python
# tags from Docker Hub.
FROM ubuntu:18.04
RUN apt-get update \
    && apt-get install -y --no-install-recommends mysql-server \
    && apt-get install -y --no-install-recommends python3.6 \
    && apt-get install -y --no-install-recommends vim \
    && apt-get install -y --no-install-recommends python3-pip \
    && rm -rf /var/lib/apt/lists/* 

ENTRYPOINT service mysql start && bash
LABEL Name=pysqln Version=0.0.1
#EXPOSE 3000

WORKDIR /code
ADD . /code
COPY requirements.txt /code

# Using pip:
RUN python3 -m pip install -r requirements.txt


