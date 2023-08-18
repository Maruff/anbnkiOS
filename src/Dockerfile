FROM debian:bullseye-backports

MAINTAINER Guy Sheffer <Maruff at gmail dot com>

RUN set -x \
    && apt-get update && apt-get install -y \
        build-essential \
        curl \
        git \
        wget \
        p7zip-full \
        python3 \
        binfmt-support \
        qemu \
        qemu-user-static/bullseye-backports \
        sudo \
        file \
        fdisk \
        btrfs-progs \
        jq \
        zip \
        xz-utils \
        lsof \
    && rm -rf /var/lib/apt/lists/*

RUN ln -s /anbnkios/nightly_build_scripts/anbnkiOS_nightly_build /usr/bin/build
RUN ln -s /usr/bin/python3 /usr/bin/python

COPY . /anbnkiOS

CMD ["/bin/bash"]
