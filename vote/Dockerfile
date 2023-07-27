# syntax=docker/dockerfile:1

FROM python:3.8-slim-buster

LABEL image.name="Python Backend"
LABEL image.version="3.8"
LABEL image.description="A Python application, which handles the operations sent from the Frontend app."
LABEL image.author="mmaziec"

WORKDIR /vote

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

EXPOSE 5000

COPY . .

CMD ["python3", "-m" , "flask", "run", "--host=0.0.0.0"]