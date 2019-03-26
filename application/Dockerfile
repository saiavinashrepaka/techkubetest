FROM maven:3.6-jdk-8-onbuild 

FROM java:8
COPY target/student-services-security-0.0.1-SNAPSHOT.jar /opt/student.jar
CMD ["java","-jar","/opt/student.jar"]
