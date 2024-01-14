FROM python:3.12.1-alpine

WORKDIR /Users/Mahammad/app

# prevent Python from writing .pyc files
ENV PYTHONDONTWRITEBYTECODE 1
# ensure Python output is sent directly to the terminal without buffering
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
COPY ./requirements.txt  requirements.txt
RUN pip install  -r requirements.txt

COPY . /Users/Mahammad/app
CMD python manage.py runserver 0.0.0.0:8000

# FROM python as python-build-stage

# 	ENV PYTHONBUFFERED = 1

# 	WORKDIR /django

# 	COPY requirements.txt requirements.txt

# 	RUN pip3 install -r requirements.txt

# 	COPY . .

# 	CMD python manage.py runserver 0.0.0.0:8000