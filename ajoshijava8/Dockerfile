# Ubuntu 18.04 with Java 8 installed
# todo: add vim, nettools for wireshark, ping, telnet, ssh

#From buildpack-deps:bionic-scm
#    add-apt-repository ppa:webupd8team/java -y && \
#    echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections && \
#    apt-get install -y oracle-java8-installer && \

From ubuntu:18.04
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y software-properties-common && \
    apt-get update && \
    apt-get install -y openjdk-8-jdk && \
    apt-get install -y vim && \
    apt-get install -y iputils-ping && \
    apt-get install -y net-tools && \
    apt-get clean

#ADD adir /usr/adir
COPY makeAFile.sh /usr/
WORKDIR /usr/
