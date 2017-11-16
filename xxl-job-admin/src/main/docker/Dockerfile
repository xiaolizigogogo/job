FROM java:latest

MAINTAINER jml

ENV VERSION @project.version@
ENV ARTIFACTID @project.artifactId@
ADD ${ARTIFACTID}-${version}.jar ${ARTIFACTID}.jar
#配置时区 
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENTRYPOINT ["java","-jar","/${ARTIFACTID}.jar","--spring.profiles.active=${ACTIVE}"]