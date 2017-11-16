FROM openjdk:latest

MAINTAINER jml

ENV VERSION @project.version@
ENV ARTIFACTID @project.artifactId@
ADD ${ARTIFACTID}-${version}.war ${ARTIFACTID}.war
#配置时区 
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENTRYPOINT ["java","-jar","/${ARTIFACTID}.war","--spring.profiles.active=${ACTIVE}"]