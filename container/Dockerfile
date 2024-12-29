FROM python:3.11-slim

WORKDIR /app

RUN apt-get update && apt-get upgrade -y
RUN apt-get install ffmpeg -y

COPY requirements.txt ./
COPY main.py ./
COPY bacana.py ./

RUN pip install -r requirements.txt

COPY example.env .env

CMD ["python", "main.py"]
