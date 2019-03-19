FROM alpine:3.4
#On part de la distribution linux Alpine version 3.4

RUN apk --update add nginx php5-fpm && \
    mkdir -p /run/nginx
#On lance les commandes ci dessus

ADD www /www
ADD nginx.conf /etc/nginx/
ADD php-fpm.conf /etc/php5/php-fpm.conf
ADD run.sh /run.sh
#Permet d'ajouter les fichiers dans le conteneur

ENV LISTEN_PORT=80
#Permet de définir les variables d'environnement

EXPOSE 80
#Permet d'informer Docker les ports d'écoute

CMD /run.sh
#La commande a execute par defaut avec le conteneur
