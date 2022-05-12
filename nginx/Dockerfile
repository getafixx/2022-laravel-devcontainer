
FROM nginx:1.21-alpine

#COPY ./conf/notthatspicy.local.conf /etc/nginx/sites-available/notthatspicy.local.conf
COPY default.conf /etc/nginx/conf.d/default.conf
#setup nginx stuff
RUN ln -s /etc/nginx/sites-available/notthatspicy.local.conf /etc/nginx/sites-enabled/notthatspicy.local.conf
#RUN ln -s /etc/nginx/sites-available/art.notthatspicy.local.conf /etc/nginx/sites-enabled/art.notthatspicy.local.conf

