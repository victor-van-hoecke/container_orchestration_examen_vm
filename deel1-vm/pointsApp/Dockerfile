FROM ghcr.io/eslih/python:3.12.0-alpine

WORKDIR /pointsApp

RUN apk add --no-cache linux-headers g++

COPY . .

RUN pip install --upgrade pip \
    && pip wheel --wheel-dir=/root/wheels -r requirements.txt

CMD ["python", "app.py"]
