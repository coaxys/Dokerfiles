FROM coaxys/oracle-jdk-8:1.8.0_72
MAINTAINER Nicolas Giard, nicolas.giard@coaxys.com

RUN mkdir -p /opt/play && cd /opt/play
RUN wget https://downloads.typesafe.com/play/1.4.1/play-1.4.1.zip
RUN unzip play-1.4.1.zip
RUN mv play-1.4.1 /opt/play/play-1.4.1
RUN chmod +x /opt/play/play-1.4.1/play
RUN update-alternatives --install /usr/bin/play play /opt/play/play-1.4.1/play 1
RUN mkdir -p /app

ENV PLAY_HOME /opt/play/play-1.4.1

EXPOSE 9000

CMD ["help"]
ENTRYPOINT ["/opt/play/play-1.4.1/play"]
