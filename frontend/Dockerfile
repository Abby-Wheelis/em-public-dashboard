FROM node:20.7.0-alpine
VOLUME /public/plots

RUN mkdir -p /public
WORKDIR /public

RUN npm i -g http-server

RUN apk update && apk upgrade busybox

COPY client /public/client
COPY *.html /public/

EXPOSE 6060
CMD ["http-server", "-p", "6060"]
