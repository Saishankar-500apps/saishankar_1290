FROM openresty/openresty:buster-fat

RUN rm -rf /etc/nginx/conf.d/default.conf \
    && rm -rf /usr/local/openresty/nginx/conf/nginx.conf

ADD conf/core.conf /usr/local/openresty/nginx/conf/nginx.conf

ADD conf/default.conf /etc/nginx/conf.d/default.conf

COPY script /root/script

RUN chmod +x /root/script/*.sh

CMD ["/usr/bin/openresty", "-g", "daemon off;"]
#cmd to execute