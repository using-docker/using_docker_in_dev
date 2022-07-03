FROM python:3.4

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi

RUN pip install --upgrade pip

RUN pip install Flask uWSGI
WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
