FROM openjdk:11

WORKDIR /app
COPY JFRconfig.jfc JFRConfig.jfc
ENV JAVA_TOOL_OPTIONS="-XX:+FlightRecorder -XX:StartFlightRecording=settings=JFRConfig.jfc,disk=true,duration=60s,filename=/app/myrecording.jfr"

ADD target/CentralStation-1.0-SNAPSHOT.jar CentralStation-1.0-SNAPSHOT.jar
CMD ["java", "-jar", "CentralStation-1.0-SNAPSHOT.jar"]
