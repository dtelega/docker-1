# Dockerfile for check init unit factory project

FROM debian:8.1

MAINTAINER dtelega <dtelega@student.unit.ua>

# Install.
RUN \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get clean && \
  apt-get install -y git nano openssh-server mailutils

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]

# docker build -t init-check .
# docker run --rm -ti init-check
