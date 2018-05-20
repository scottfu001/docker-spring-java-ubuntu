# docker-spring-java8-ubuntu
Java 8 image for Spring application


docker-compose example

     app:
        image: scottfu/docker-spring-java8-ubuntu
        container_name: app
        restart: on-failure
        ports:
            - "8080:8080"
        environment:
            - TZ=Asia/Hong_Kong
            - JAR_NAME=spring-boot.jar
            - JAVA_OPTIONS=-Dfile.encoding=UTF-8
        volumes:
            - ".:/app"
        stdin_open: true
        tty: true
