FROM debian

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y wget default-jre

WORKDIR minecraft
RUN wget https://launcher.mojang.com/mc/game/1.13/server/d0caafb8438ebd206f99930cfaecfa6c9a13dca0/server.jar
EXPOSE 25565
CMD echo eula=true > eula.txt && java -Xmx1024M -Xms1024M -jar server.jar


# docker run --rm -d -p 25565:25565 --name minecraft-server bonus02 
