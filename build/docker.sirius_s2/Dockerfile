FROM tfeuvrier/sirius_dockerfile:sirius
LABEL maintainer="CS SI"

ENV DEBIAN_FRONTEND noninteractive

# ------------
# Install SIRIUS S2
#-------------
COPY sirius_s2 /opt/sirius_s2

WORKDIR /opt/sirius_s2

# -------------------
# Install lib PYTHON
# -------------------
#RUN python3 -m pip install --upgrade pip \
# && python3 -m pip install setuptools \
# && python3 -m pip install lxml rasterio

# -----------------------------
# Set variable environnement
# -----------------------------
ENV SHELL /bin/bash

#ENTRYPOINT ["python3", "/opt/sirius_s2/zoom_S2.py"]
