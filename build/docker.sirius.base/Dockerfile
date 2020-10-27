FROM osgeo/gdal:latest
LABEL maintainer="CS SI"

ENV DEBIAN_FRONTEND noninteractive

RUN echo "Europe/Paris" > /etc/timezone

# ------------------------------
# Needed packages for next step
# ------------------------------
RUN apt-get update -y \
 && apt-get upgrade -y \
 && apt-get install -y apt-transport-https software-properties-common python3-software-properties

# -----------------
# Standard packages
# -----------------
RUN apt-get update -y \
 && apt-get install -y --no-install-recommends --allow-unauthenticated \
    ca-certificates wget \
    build-essential \
    gcc \
    g++-7 \
    libfftw3-dev \
    cmake \
    python3-pip \
    python3-dev \
    python3-numpy \
    git
