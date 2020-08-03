FROM java:6
MAINTAINER GAMACORE info@gamacore.ma
RUN cd /tmp
#RUN wget --no-check-certificate https://www.mederp.net/downloads/tomcat-7.tar.gz
RUN curl https://www.mederp.net/downloads/tomcat-7.tar.gz --output tomcat-7.tar.gz
RUN tar xvf tomcat-7.tar.gz -C /tmp
RUN rm -rf  tomcat-7.tar.gz
RUN mv /tmp/tomcat /opt
WORKDIR /opt/tomcat

EXPOSE 8080

CMD ["./bin/catalina.sh", "run"]

# construire avec : docker build -t tomcat6mederp .
# lancer avec : docker run -p 5555:8080 -v /tmp/webapps:/opt/tomcat/webapps -d --name tomcat.advanceeur tomcat6mederp
