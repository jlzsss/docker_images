FROM centos:7

MAINTAINER LG <endoffight@gmail.com>

# ustc
ENV YUM_BOOST_URL https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3

# mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup 
# curl -o /etc/yum.repos.d/CentOS-Base.repo https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3

RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup && \
        curl -o /etc/yum.repos.d/CentOS-Base.repo $YUM_BOOST_URL
# update
ONBUILD RUN yum update -y && yum clean all

# pip
ENV PIP_URL https://bootstrap.pypa.io/get-pip.py
# curl -o /get-pip.py https://bootstrap.pypa.io/get-pip.py && python /get-pip.py && rm /get-pip.py
RUN curl -o /get-pip.py $PIP_URL && python /get-pip.py && rm /get-pip.py

CMD ["bash"]