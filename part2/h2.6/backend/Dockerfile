FROM ubuntu:18.04
WORKDIR /app
COPY logs.txt .
ENV REDIS=localhost
RUN apt-get update && apt-get install -y curl
RUN apt-get update && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs
RUN node -v && npm -v
RUN git clone https://github.com/docker-hy/backend-example-docker.git
CMD cd backend-example-docker && npm install && FRONT_URL=http://localhost:5000 npm start
