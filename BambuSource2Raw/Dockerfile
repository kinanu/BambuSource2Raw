FROM ubuntu:20.04 as build
RUN apt-get update && apt-get install -y unzip libcurl4 libcurl4-openssl-dev wget build-essential
RUN mkdir /bambusource2raw
WORKDIR /bambusource2raw
COPY BambuSource2Raw /bambusource2raw
RUN make -f Makefile.linux

#FROM build as image
#RUN apt-get update && apt-get install -y curl iputils-ping
#RUN mkdir -p /bambu-bin
#RUN mkdir -p /bambu-bin/cfg
#WORKDIR /bambu-bin
#COPY bambusource2raw /bambu-bin/bambusource2raw
#COPY start_rtsp_feed_docker.sh /bambu-bin/start_rtsp_feed_docker.sh
#COPY ffmpeg /bambu-bin/ffmpeg
#COPY rtsp-simple-server /bambu-bin/rtsp-simple-server
#COPY rtsp-simple-server.yml /bambu-bin/rtsp-simple-server.yml
#COPY libBambuSource.so /bambu-bin/libBambuSource.so
#EXPOSE 8554
#CMD ["/bin/bash", "/bambu-bin/start_rtsp_feed_docker.sh"]
