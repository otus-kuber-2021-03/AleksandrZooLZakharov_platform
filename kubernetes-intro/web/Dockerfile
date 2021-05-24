FROM nginx:1.19.6
RUN useradd -d /app -u 1001 ungi && \
    chown -R ungi /var/cache/nginx && \
    chown -R ungi /var/run/ && \
    rm -f /etc/nginx/nginx.conf && \
    echo 'events {\n\
    worker_connections   1024;\n\
}\n\
\n\
http {\n\
    server {\n\
        listen 8000;\n\
        root /app;\n\
    }\n\
}' > /etc/nginx/nginx.conf
USER 1001
