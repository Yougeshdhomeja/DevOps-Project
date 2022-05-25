FROM php:7.3.3-apache
RUN apt-get update && apt-get install -y gnupg2
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 112695A0E562B32A
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 54404762BBB6E853
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys DCC9EFBF77E11517
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 648ACFD622F3D138
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9

RUN apt-get update && apt-get upgrade -y

RUN docker-php-ext-install mysqli
EXPOSE 80
