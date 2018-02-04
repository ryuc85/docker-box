FROM amd64/alpine:3.7
RUN apk update && apk upgrade
RUN apk add tzdata
COPY /usr/share/zoneinfo/Asia/Tokyo /etc/localtime
RUN echo "Asia/Tokyo" >> /etc/timezone
RUN apk del tzdata
