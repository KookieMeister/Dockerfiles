FROM amazoncorretto:8
RUN mkdir /opt/minecraft
WORKDIR /opt/minecraft
RUN yum clean all && yum update -y
RUN yum install wget unzip -y
RUN wget https://launcher.mojang.com/v1/objects/35139deedbd5182953cf1caa23835da59ca3d7cd/server.jar
RUN echo 'eula=True' >> /opt/minecraft/eula.txt
CMD java -server -Xmx$MINECRAFT_XMX -jar server.jar nogui