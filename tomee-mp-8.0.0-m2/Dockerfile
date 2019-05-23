FROM openjdk:11-jre-slim

LABEL maintainer="David Salter <wedevelopinjava@gmail.com>"

RUN apt-get update
RUN apt-get -y install wget

RUN wget http://apache.mirrors.nublue.co.uk/tomee/tomee-8.0.0-M2/apache-tomee-8.0.0-M2-microprofile.tar.gz

RUN tar xvzf apache-tomee-8.0.0-M2-microprofile.tar.gz -C /opt

RUN rm -rf /opt/apache-tomee-microprofile-8.0.0-M2/webapps/

ENV DEPLOY_DIR /opt/apache-tomee-microprofile-8.0.0-M2/webapps/

EXPOSE 8080

CMD ["/opt/apache-tomee-microprofile-8.0.0-M2/bin/catalina.sh", "run"]
