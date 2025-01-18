FROM debian:buster

RUN apt-get update -y && apt-get upgrade -y

RUN apt install nginx openssl -y

COPY ./conf/default.conf /etc/nginx/sites-available/

EXPOSE 443

WORKDIR /run

COPY ./tools/run.sh .

RUN chmod +x run.sh

CMD ["./run.sh"]
