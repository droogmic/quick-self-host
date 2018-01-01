# Nginx reverse proxy
based on: https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion/blob/master/docker-compose-multiple-networks.yml

## Guide
+ Set .env
+ Setup other containers as described in [main README]
+ Authelia customisation - nginx-data/vhost.d
  + edit auth_location with domain name
  + add service.example.duckdns.org and service.example.duckdns.org_location for every service needing authelia protection

## TODO
+ Move NGINX_FILES_PATH to named volumes

## Resources
https://github.com/jwilder/nginx-proxy
https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion

[main README]: ../
