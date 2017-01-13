FROM debian:jessie

MAINTAINER LG <endoffight@gmail.com>

# mirror
sed -i 's/httpredir.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list

# update
ONBUILD RUN apt-get update && apt-get -y upgrade

# pip
ENV PIP_URL https://bootstrap.pypa.io/get-pip.py
# curl -o /get-pip.py https://bootstrap.pypa.io/get-pip.py && python /get-pip.py && rm /get-pip.py
RUN curl -o /get-pip.py $PIP_URL && python /get-pip.py && rm /get-pip.py

CMD ["bash"]