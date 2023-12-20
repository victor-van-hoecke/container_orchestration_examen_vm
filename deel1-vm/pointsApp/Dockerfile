FROM ghcr.io/eslih/python:3.12.0-alpine

WORKDIR /pointsApp

# Install system dependencies
RUN apk add --no-cache linux-headers g++

# Install Python dependencies
COPY requirements.txt ./
RUN pip install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY . .

CMD ["python", "app.py"]
