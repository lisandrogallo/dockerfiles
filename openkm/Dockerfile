FROM ubuntu:16.04
CMD /bin/bash
MAINTAINER lisogallo
ENV CATALINA_HOME=/usr/local/tomcat
ENV TOMCAT_VERSION=7.0.61
ENV JAVA_HOME=/usr/local/java
ENV ORACLE_JAVA_HOME=/usr/lib/jvm/java-7-oracle/
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections && apt-get install -y software-properties-common && add-apt-repository -y ppa:webupd8team/java && apt-get update && apt-get install -y oracle-java7-installer
RUN ln -s $ORACLE_JAVA_HOME $JAVA_HOME
RUN apt-get -y install libreoffice imagemagick swftools liblog4j1.2-java libgnumail-java ant curl unzip sudo tar tesseract-ocr tesseract-ocr-eng tesseract-ocr-spa poppler-utils --no-install-recommends
RUN curl -L https://downloads.sourceforge.net/project/openkm/6.3.1/openkm-6.3.1-community-tomcat-bundle.zip -o /usr/local/openkm-tomcat-bundle.zip && unzip /usr/local/openkm-tomcat-bundle.zip -d /usr/local/ && rm /usr/local/openkm-tomcat-bundle.zip && ln -s $CATALINA_HOME /opt/openkm
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/tomcat/bin
EXPOSE 2002/tcp 8080/tcp
CMD "/bin/sh" "-c" "/usr/local/tomcat/bin/catalina.sh run"
