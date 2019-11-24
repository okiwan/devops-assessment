FROM python:3.7.3

RUN apt-get update
COPY . /app
RUN cd /app && python setup.py install

ADD docker/entrypoint.sh /entrypoint.sh
ADD docker/prepare_env.sh /app/prepare_env.sh

WORKDIR /app
EXPOSE 5000
ENTRYPOINT ["/entrypoint.sh"]
