FROM debian:jessie

MAINTAINER LG <endoffight@gmail.com>

# mirror
RUN sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list\
    && sed -i 's|security.debian.org|mirrors.ustc.edu.cn/debian-security|g' /etc/apt/sources.list

RUN apt-get update -qq &&\
        apt-get -qqy upgrade &&\
        apt-get install -qqy --no-install-recommends\
        ca-certificates\
        curl\
        wget\
        python\
        apt-utils\
        dialog\
        debconf-utils\
        tzdata\
        unzip &&\
        apt-get clean &&\
        rm -rf /var/lib/apt/lists/* &&\
        echo "Asia/Shanghai" > /etc/timezone &&\
        dpkg-reconfigure -f noninteractive tzdata &&\
        echo 'alias ll="ls -lah --color=auto"' >> /etc/bash.bashrc

# pip
ENV PIP_URL https://bootstrap.pypa.io/get-pip.py

RUN wget $PIP_URL && python get-pip.py && rm get-pip.py

CMD ["bash"]