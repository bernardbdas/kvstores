FROM redis/redis-stack:latest as redis
ENV CONF_PATH=.docker/redis/redis.conf
ENV ACL_PATH=.docker/redis/users.acl
COPY ${CONF_PATH} /usr/local/etc/redis/
COPY ${ACL_PATH} /usr/local/etc/redis/
RUN chmod 777 -R /usr/local/etc/redis/
EXPOSE 6379 8001
# CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]
ENTRYPOINT [ "redis-server", "/etc/redis/redis.conf" ]
HEALTHCHECK NONE