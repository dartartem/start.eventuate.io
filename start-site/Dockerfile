FROM openjdk:11.0.6-jre-slim-buster
RUN apt-get update && apt-get install -y curl
HEALTHCHECK --start-period=30s --interval=5s CMD curl -f http://localhost:8080/actuator/health || exit 1
CMD java ${JAVA_OPTS} -jar start-site-exec.jar
COPY target/start-site-exec.jar .
