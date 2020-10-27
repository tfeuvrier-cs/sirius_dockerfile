FROM tfeuvrier/sirius_dockerfile:sirius
LABEL maintainer="CS SI"

ENV DEBIAN_FRONTEND noninteractive

# ------------
# Install SIRIUS S2
#-------------
COPY sirius_s2 /opt/sirius_s2

# ------------
# SET ENTRYPOINT
# ------------
ENTRYPOINT ["python3", "/opt/sirius_s2/zoom_S2.py"]
