FROM centos:7

MAINTAINER LG <endoffight@gmail.com>

# repo
RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup &&\
         curl -o /etc/yum.repos.d/CentOS-Base.repo https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3
# update
RUN yum update -y && yum install -y wget git &&\
        yum groupinstall -y "Development Tools" &&\
        yum clean all &&\
        echo 'Asia/Shanghai' > /etc/timezone

# pip
RUN wget https://bootstrap.pypa.io/get-pip.py && python get-pip.py && rm get-pip.py

CMD ["bash"]