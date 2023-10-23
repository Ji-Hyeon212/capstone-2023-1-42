FROM openjdk:11-jdk

ARG JAR_FILE=build/libs/*.jar
COPY ${JAR_FILE} app.jar

ENV MYSQL_ID "root"
ENV MYSQL_PASSWORD "donu123"
ENV MYSQL_URL "jdbc:mysql://3.39.150.229:3306/tayotayo_DB?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=Asia/Seoul&characterEncoding=UTF-8"
ENV TAYOTAYO_S3_ACCESS_KEY "AKIA3SX3OFPVDSHOS62E"
ENV TAYOTAYO_S3_NAME "my.tayotayo.sss.bucket"
ENV TAYOTAYO_S3_SECRET_KEY "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"

ENTRYPOINT ["java","-jar","/app.jar"]