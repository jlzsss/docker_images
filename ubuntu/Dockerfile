FROM ubuntu:zesty

MAINTAINER LG <endoffight@gmail.com>

# timezone
RUN echo 'Asia/Shanghai' > /etc/timezone

#RUN sed -i "s/archive\.ubuntu\.com/mirrors\.163\.com/g" /etc/apt/sources.list
#RUN sed -i "s/archive\.ubuntu\.com/mirrors\.aliyun\.com/g" /etc/apt/sources.list
#RUN sed -i "s/archive\.ubuntu\.com/tw\.archive\.ubuntu\.com/g" /etc/apt/sources.list
#RUN sed -i "s/archive\.ubuntu\.com/cn\.archive\.ubuntu\.com/g" /etc/apt/sources.list
RUN sed -i "s/archive\.ubuntu\.com/mirrors\.ustc\.edu\.cn/g" /etc/apt/sources.list

CMD ["bash"]