FROM debian:buster

LABEL maintainer="Roh yeon jin(zacronan@naver.com)"
RUN apt-get update && apt-get install -y nginx nginx-extras

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./entrypoint.sh /etc/nginx/entrypoint.sh

RUN rm -rf /etc/nginx/sites-enabled/default
WORKDIR /etc/nginx 

RUN chmod +x ./entrypoint.sh
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]