FROM wordpress:latest

VOLUME /etc/letsencrypt /var/lib/letsencrypt

RUN apt-get update && \
        apt-get install -y  --no-install-recommends ssl-cert wget && \
        rm -r /var/lib/apt/lists/* && \
        a2enmod ssl && \
        a2ensite default-ssl

RUN wget https://dl.eff.org/certbot-auto && \
        chmod a+x certbot-auto

EXPOSE 80
EXPOSE 443
