FROM tomcat:latest

MAINTAINER jml

ENV VERSION @project.version@
ENV ARTIFACTID @project.artifactId@
RUN rm -rf /usr/local/tomcat/webapps/
RUN mkdir /usr/local/tomcat/webapps/
ADD ${ARTIFACTID}-${version}.war /usr/local/tomcat/webapps/ROOT.war
#配置时区 
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

