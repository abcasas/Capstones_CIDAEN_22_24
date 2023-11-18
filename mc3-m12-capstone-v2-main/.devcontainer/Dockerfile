FROM python:3.11.4-bullseye

USER root

# Install java

RUN apt-get update && apt-get install -y \
    openjdk-11-jdk \
    openjdk-11-jre \
    && rm -rf /var/lib/apt/lists/*

# Install pip requirements 

COPY requirements.txt /tmp/
RUN pip --no-cache-dir install -r /tmp/requirements.txt 

RUN mkdir -p /work
WORKDIR /work