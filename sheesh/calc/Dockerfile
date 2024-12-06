FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    openjdk-11-jre \
    x11-apps \
    xauth \
    libfreetype6 \
    fontconfig \
    && rm -rf /var/lib/apt/lists/*

ENV DISPLAY=host.docker.internal:0

COPY calc.jar /app/calc.jar

WORKDIR /app

CMD ["java", "-jar", "calc.jar"]
