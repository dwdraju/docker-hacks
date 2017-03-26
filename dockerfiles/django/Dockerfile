FROM ubuntu:14.04

MAINTAINER Raju Dawadi <rajudawadinp@gmail.com>

# Set the enviroment variable
ENV DEBIAN_FRONTEND noninteractive

# Install required packages
RUN apt-get update
RUN apt-get -y install build-essential python-dev libmysqlclient-dev python-virtualenv

RUN virtualenv venv --no-site-packages
RUN . /venv/bin/activate; \
	pip install django==1.5 mysql-python suds-jurko django-debug-toolbar==1.0.1 XlsxWriter sqlparse==0.1.19 South;\
	pip install --upgrade setuptools

ADD ./ /django

RUN chmod 755 /django/*.sh