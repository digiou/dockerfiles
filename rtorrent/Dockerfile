FROM alpine:edge
MAINTAINER Dimitrios Giouroukis <dimitrios.giouroukis@gmail.com>

RUN adduser -D rtorrent

COPY ./.rtorrent.rc /home/rtorrent/

ENV TERM xterm

RUN apk add --no-cache rtorrent && \
    mkdir /home/rtorrent/.session /data /data/comple /data/incomplete /data/watch && \
    chown -R rtorrent:rtorrent /home/rtorrent/ /data

VOLUME ["/data/complete", "/data/incomplete", "/data/watch"]

EXPOSE 51413

USER rtorrent
CMD ["rtorrent"]
