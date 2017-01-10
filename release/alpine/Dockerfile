FROM alpine:3.4

ENV PACKAGES "lighttpd perl perl-encode"

RUN apk add --update $PACKAGES \
    && rm -rf /var/cache/apk/*
ADD lighttpd.conf /etc/lighttpd/lighttpd.conf
RUN adduser www-data -G www-data -H -s /bin/false -D

EXPOSE 80
VOLUME /var/www
#https://wiki.alpinelinux.org/wiki/Dglog
#ENTRYPOINT ["/usr/sbin/lighttpd", "-D", "-f", "/etc/lighttpd/lighttpd.conf"]
