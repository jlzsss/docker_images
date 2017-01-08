FROM centos:7

MAINTAINER endoffight@gmail.com

ENV YUM_BOOST_URL https://lug.ustc.edu.cn/wiki/_export/code/mirrors/help/centos?codeblock=3

RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup && \
        curl -o /etc/yum.repos.d/CentOS-Base.repo $YUM_BOOST_URL

RUN yum clean all && yum update -y && yum clean all

ENV PIP_URL https://raw.github.com/pypa/pip/master/contrib/get-pip.py

RUN curl -o /get-pip.py $PIP_URL && python /get-pip.py && rm /get-pip.py

CMD ["bash"]