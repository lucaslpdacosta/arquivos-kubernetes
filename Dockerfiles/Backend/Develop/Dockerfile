FROM node:latest

WORKDIR /app

RUN apt-get update && apt-get upgrade -y && apt-get install git -y

RUN git clone https://github.com/lucaslpdacosta/nuvem-backend.git .

EXPOSE 3000

CMD ["bash", "-c", "git checkout develop && git pull origin develop && npm install && node index.js"]