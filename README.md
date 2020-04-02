# docker-antmedia-server
https://github.com/ant-media/Ant-Media-Server/releases/download/ams-v1.9.1/ant-media-server-1.9.1-community-1.9.1-20200112_1622.zip

docker build --network=host -t antmedia-server/latest --build-arg AntMediaServer=ant-media-server-1.9.1-community-1.9.1-20200112_1622.zip ./docker