# Koristimo zvanicni Docker image za Java 11
FROM adoptopenjdk:11-jre-hotspot

# Postavljamo radni direktorijum unutar kontejnera
WORKDIR /app

#VOLUME /tmp
EXPOSE 8080

# Kopiramo JAR fajl aplikacije u radni direktorijum
# COPY target/demo-0.0.1-SNAPSHOT.jar application.jar
ARG JAR_FILE=target/demo-0.0.1-SNAPSHOT.jar
ADD ${JAR_FILE} application.jar

# Pokrećemo Spring Boot aplikaciju prilikom startovanja kontejnera
# CMD ["java", "-jar", "application.jar"]
ENTRYPOINT ["java", "-jar", "application.jar"]