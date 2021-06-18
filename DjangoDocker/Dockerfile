FROM python:3.9.5-slim
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code
COPY requirements.txt /code/
RUN pip install --user -r requirements.txt
#COPY . /code/
# Use this command if you use bind mount
#WINDOWS: docker run --mount src=%cd%,target=/code,type=bind -p 8001:8000 -it --rm django-dev
#LINUX: docker run --mount src="${pwd}",target=/code,type=bind -p 8001:8000 -it --rm django-dev
CMD python manage.py runserver 0.0.0.0:8000