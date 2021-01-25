FROM amazoncorretto:8
RUN mkdir /opt/minecraft
WORKDIR /opt/minecraft
RUN yum clean all && yum update -y
RUN yum install wget unzip -y
RUN wget http://solder.endermedia.com/repository/downloads/the-1122-pack/the-1122-pack_1.3.0.zip && unzip the-1122-pack_1.3.0.zip
RUN echo 'eula=True' >> /opt/minecraft/eula.txt
CMD java -server -Xmx6G -Dfml.queryResult=confirm -jar forge-1.12.2-14.23.5.2854.jar nogui