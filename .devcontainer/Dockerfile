FROM ubuntu:22.04

# Setting timezone to Montreal for PHP installation
ENV TZ=America/Montreal
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update \
    && apt-get -y install git software-properties-common \
    && add-apt-repository ppa:ondrej/php \
    && apt install php8.2 php8.2-pgsql -y