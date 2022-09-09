FROM nginx:latest

# computer environment
ENV TZ=UTC

# packages
RUN apt-get update

# timezone
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

# working directory
WORKDIR /var/www/html
