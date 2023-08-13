
FROM nginx:latest
RUN apt-get update
RUN apt-get install vim
RUN chmod 644 /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY default.conf /etc/nginx/nginx.conf
ADD static /usr/share/nginx/html/
RUN rm -rf /usr/share/nginx/html/index.html
ENV CATALOGUE_HOST="catalogue"


