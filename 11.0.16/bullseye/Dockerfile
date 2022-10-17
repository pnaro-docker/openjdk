FROM debian:bullseye
RUN apt-get update \
  && apt-get install postgis=3.1.1+dfsg-1 -y \
  && apt-get remove postgresql-13 -y \
  && apt-get autoremove -y \
  && apt-get install openjdk-11-jre=11.0.16+8-1~deb11u1 -y \
  && apt-get clean

ENV JAR_FILE_NAME=app.jar
WORKDIR /app
CMD "java" "-XX:MaxRAMPercentage=80.0" "-jar" "${JAR_FILE_NAME}"
