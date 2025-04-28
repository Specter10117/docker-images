FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /minecraft

RUN apt-get update && apt-get install -y \
    openjdk-17-jdk \
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN wget -O uberbukkit-2.0.2.jar https://github.com/Moresteck/uberbukkit/releases/download/2.0.2-241217-1442-3a5552b/uberbukkit-2.0.2.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

CMD [ "-Xmx1024M", "-Xms1024M", "-jar", "uberbukkit-2.0.2.jar", "nogui" ]

ENTRYPOINT [ "java" ] 
