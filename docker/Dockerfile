FROM ubuntu:16.04

ARG AntMediaServer

RUN apt-get update 
RUN apt-get install -y libx11-dev
RUN apt-get install -y wget

ADD ./${AntMediaServer} /home

RUN cd home \
    && pwd \
    && wget https://raw.githubusercontent.com/ant-media/Scripts/master/install_ant-media-server.sh \
    && chmod 755 install_ant-media-server.sh

RUN cd home \
    && pwd \
    && wget https://github.com/ant-media/Ant-Media-Server/releases/download/ams-v1.9.1/ant-media-server-1.9.1-community-1.9.1-20200112_1622.zip \
    && ./install_ant-media-server.sh ${AntMediaServer}

ENTRYPOINT service antmedia start && bash