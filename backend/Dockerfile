FROM python:3.7.14-slim

WORKDIR /usr/src/app
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
RUN apt-get -y update && apt-get install -y libzbar-dev libpq-dev python-dev graphviz pkg-config libgraphviz-dev build-essential
RUN pip install --upgrade pip
COPY /requirements.txt /usr/src/app/
RUN pip install -r requirements.txt
COPY . /usr/src/app/
EXPOSE 8000
CMD ["python","manage.py","runserver","0.0.0.0:8000"]

