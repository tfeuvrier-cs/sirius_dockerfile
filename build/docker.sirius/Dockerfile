FROM tfeuvrier/sirius_dockerfile:sirius.base
LABEL maintainer="CS SI"

ENV DEBIAN_FRONTEND noninteractive

COPY . /tmp/sources/

RUN export SIRIUS_VERSION=0.2.0 \
    && cd /tmp/sources/ \
    && mkdir .build \
    && cd .build \
    && cmake .. \
        -G "Unix Makefiles" \
        -DCMAKE_BUILD_TYPE=Release \
        -DCMAKE_INSTALL_PREFIX=/opt/sirius \
        -DSIRIUS_VERSION="${SIRIUS_VERSION}" \
        -DENABLE_CACHE_OPTIMIZATION=ON \
        -DENABLE_GSL_CONTRACTS=OFF \
        -DENABLE_LOGS=ON \
        -DBUILD_TESTING=OFF \
        -DWITH_PYTHON=OFF \
        -DENABLE_DOCUMENTATION=ON \
    && make -j4 libsirius \
    && make -j4 libsirius-static \
    && make -j4 sirius \
    && make install

RUN rm -rf /tmp/sources
