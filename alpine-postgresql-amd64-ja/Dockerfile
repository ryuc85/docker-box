FROM amd64/alpine:3.7
RUN apk update && apk upgrade && \
apk add tzdata
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
echo "Asia/Tokyo" > /etc/timezone && \
apk del tzdata
RUN apk add postgresql && \
mkdir /run/postgresql && chown postgres:postgres /run/postgresql && \
mkdir /data && chown postgres:postgres /data
RUN su - postgres -c 'initdb /data' && \
su - postgres -c 'export PGDATA=/data && pg_ctl start'
