FROM openjdk:11.0.9.1


VOLUME /tmp

COPY /target/docker-mysql-springboot-demo-0.0.1-SNAPSHOT.jar docker-mysql-springboot-demo-0.0.1-SNAPSHOT.jar

COPY wait-for-mysql.sh /wait-for-mysql.sh

RUN chmod +x /wait-for-mysql.sh

ENTRYPOINT ["sh", "-c", "/wait-for-mysql.sh && java -jar /docker-mysql-springboot-demo-0.0.1-SNAPSHOT.jar"]
