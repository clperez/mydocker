FROM node:latest
RUN apt-get update && \
    apt-get install -y python3 && \
    apt-get install -y python3-pip && \
    npm install -g nodemon
WORKDIR /app
COPY requirements.txt ./
RUN pip3 install -r requirements.txt
COPY . .
CMD nodemon --legacy-watch --exec python3 main.py
