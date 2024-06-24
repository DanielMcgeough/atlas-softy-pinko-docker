# Use the latest version of Ubuntu as a base image
FROM ubuntu:22.04
# Update APT package list
RUN apt-get update
# Upgrade all installed packages
RUN apt-get upgrade -y
# Install Python3, Flask and pip3
RUN apt-get install -y python3 python3-pip
RUN pip3 install flask
# list the working directory
WORKDIR /app
# copy files
COPY  ./api.py /app/api.py
# Port to use
EXPOSE 5252
