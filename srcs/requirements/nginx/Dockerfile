FROM debian:bullseye

RUN apt-get update
RUN apt-get install -y \
  nginx \
  openssl \
  && rm -rf /var/lib/apt/lists/*

RUN rm /etc/nginx/sites-enabled/default
COPY conf/nginx.conf /etc/nginx/sites-enabled/

RUN mkdir -p /etc/nginx/ssl && openssl req -x509 \
            -sha256 -days 356 \
            -nodes \
            -newkey rsa:2048 \
            -subj "/CN=viburton.42.fr/C=FR/L=Paris/O=viburton@42" \
            -keyout /etc/nginx/ssl/inception.key -out /etc/nginx/ssl/inception.crt

ENTRYPOINT ["nginx", "-g", "daemon off;"]
