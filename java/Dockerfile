## Reference: https://github.com/iPraBhu/ADevGuide/tree/master/SimpleJavaProject
FROM maven:3.5.4-jdk-8 as maven
RUN apt install -y git
RUN git clone https://github.com/iPraBhu/ADevGuide.git
WORKDIR /ADevGuide/SimpleJavaProject
RUN mvn dependency:go-offline -B
RUN mvn package

# FROM openjdk:8-jdk-alpine
# WORKDIR /app
# VOLUME /tmp
# ARG JAVA_OPTS
# ENV JAVA_OPTS=$JAVA_OPTS
# COPY --from=maven target/SimpleJavaProject-*.jar ./app/SimpleJavaProject.jar
# EXPOSE 3000
# ENTRYPOINT exec java $JAVA_OPTS -jar app/SimpleJavaProject.jar
# For Spring-Boot project, use the entrypoint below to reduce Tomcat startup time.
#ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar dockersamplesbylang.jar
