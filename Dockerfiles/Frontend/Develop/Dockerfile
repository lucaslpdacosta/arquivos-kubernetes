FROM nginx:latest

WORKDIR /app

RUN rm /etc/nginx/conf.d/default.conf

COPY default.conf /etc/nginx/conf.d/default.conf

RUN apt-get update && apt-get upgrade -y && apt-get install git -y

RUN git clone https://github.com/lucaslpdacosta/nuvem-frontend.git .

EXPOSE 80

CMD ["bash", "-c", "git checkout develop && git pull origin develop && nginx -g 'daemon off;'"]