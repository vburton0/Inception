FROM debian:buster

# Install Nginx
# Update the package list and install nginx and -y flag to avoid prompt
RUN apt update                  
RUN apt install -y nginx        

# Install tools
RUN apt install vim -y          
RUN apt install curl -y

# Certificates : create a self-signed certificate
RUN mkdir -p /etc/nginx/ssl
RUN apt install openssl -y
RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=IDF/L=Paris/O=42/OU=42/CN=login.42.fr/UID=login"

# Copy the configuration file
COPY conf/nginx.conf /etc/nginx/nginx.conf