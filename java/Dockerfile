#loongnix with openjdk8
#huanwei/loongnix-openjdk8
FROM loongnix/loongnix-base:latest
MAINTAINER Huan Wei <huan@harmonycloud.cn>

ENV JAVA_PKG=jdk8-mips64-8.1.tar.gz

RUN yum install -y tar \
 && yum clean all -y

RUN curl http://ftp.loongnix.org/toolchain/java/openjdk8/${JAVA_PKG} -o ${JAVA_PKG} \
 && tar zxvf ${JAVA_PKG} -C /opt \
 && rm -rf ${JAVA_PKG}

ENV PATH=/opt/j2sdk-image/bin/:$PATH

RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
 && echo 'Asia/Shanghai' > /etc/timezone