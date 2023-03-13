FROM nginx

RUN openssl genrsa -out /etc/ssl/private/myhostname.key 4096
RUN openssl req -new -key /etc/ssl/private/myhostname.key -out myhostname.csr -subj "/C=US/ST=New York/L=New York/O=My Company/OU=My Department/CN=myhostname.com"
RUN cp /etc/ssl/private/myhostname.key myhostname.key.pw
RUN openssl rsa -in myhostname.key.pw -out /etc/ssl/private/myhostname.key
RUN openssl x509 -req -in myhostname.csr -signkey /etc/ssl/private/myhostname.key -out myhostname.crt
RUN mkdir /etc/nginx/ssl
RUN cp myhostname.crt /etc/nginx/ssl
RUN cp /etc/ssl/private/myhostname.key /etc/nginx/ssl

COPY addtodefault.conf addtodefault.conf
RUN cat addtodefault.conf >> /etc/nginx/conf.d/default.conf
