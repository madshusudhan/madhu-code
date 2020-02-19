FROM openjdk:8-jdk-alpine
RUN apk --no-cache add curl
COPY target/micronaut-groovy-service*.jar micronaut-groovy-service.jar
#COPY build/libs/*-all.jar micronaut-groovy-service.jar
EXPOSE 8080
CMD java -XX:+UnlockExperimentalVMOptions -XX:+UseCGroupMemoryLimitForHeap \
    -Dcom.sun.management.jmxremote -noverify ${JAVA_OPTS} -jar micronaut-groovy-service.jar
