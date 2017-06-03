FROM buildpack-deps:jessie

ENV KT_VERSION 1.1.2-2

RUN apt-get update
RUN apt-get install -y default-jdk 

ENV KT_PACKAGE_URL https://github.com/JetBrains/kotlin/releases/download/v1.1.2-2/kotlin-compiler-${KT_VERSION}.zip
RUN apt-get install -y unzip
RUN wget $KT_PACKAGE_URL -O /tmp/a.zip && unzip /tmp/a.zip -d /opt && rm /tmp/a.zip
ENV PATH $PATH:/opt/kotlinc/bin
