FROM alpine:edge
MAINTAINER Dimitrios Giouroukis <dimitrios.giouroukis@gmail.com>

RUN echo "@testing http://nl.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk add --no-cache py-pygments hugo@testing

EXPOSE 1313
CMD ["hugo", "version"]
