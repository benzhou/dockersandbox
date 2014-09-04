FROM ubuntu:14.04
MAINTAINER BEN ZHOU <amailtoaben@gmail.com>

RUN apt-get update && apt-get install -y software-properties-common
RUN add-apt-repository ppa:webupd8team/java -y

#JAVA GIT
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections
RUN apt-get update && apt-get install -y oracle-java7-installer git

#Maven
RUN wget http://www.carfab.com/apachesoftware/maven/maven-3/3.2.3/binaries/apache-maven-3.2.3-bin.tar.gz -P /tmp/
RUN mkdir /usr/local/apache-maven
RUN tar -xvzf /tmp/apache-maven-3.2.3-bin.tar.gz -C /usr/local/apache-maven
RUN export M2_HOME=/usr/local/apache-maven/apache-maven-3.2.3
RUN export M2=$M2_HOME/bin
RUN export MAVEN_OPTS="-Xms256m -Xmx512m"
RUN export PATH=$M2:$PATH


