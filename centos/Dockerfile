FROM centos:7

MAINTAINER LG <endoffight@gmail.com>

RUN echo 'Asia/Shanghai' > /etc/timezone

# ustc
ENV YUM_BOOST_URL https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3

# mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup 
# curl -o /etc/yum.repos.d/CentOS-Base.repo https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3

RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup &&\
         curl -o /etc/yum.repos.d/CentOS-Base.repo $YUM_BOOST_URL
# update
ONBUILD RUN yum update -y && yum install -y wget && yum clean all

# pip
RUN wget https://bootstrap.pypa.io/get-pip.py && python get-pip.py && rm get-pip.py

CMD ["bash"]