FROM python:3.4

RUN pip install Flask==0.10.1 uWSGI==2.0.8
WORKDIR /app
COPY app /app

CMD ["uwsgi", "--http", "0.0.0.0:9090", "--wsgi-file", "/app/identidock.py", \
     "--callable", "app", "--stats", "0.0.0.0:9191"]
