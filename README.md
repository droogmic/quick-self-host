# Quick Self Host

## Core functionality
+ Nginx reverse proxy - https://github.com/jwilder/nginx-proxy
+ Authelia authenitcation of unauthenticated services - https://github.com/clems4ever/authelia
+ LDAP directory service for SSO - https://github.com/osixia/docker-openldap

## TODO
+ Fix 2FA with Authelia - currently only 1FA works, on trying to register 2FA authelia raises a 401 error
+ Refactor reverse proxy
+ Standardise config structure

## Guide
This walks through setting up LDAP, reverse proxy and authelia with an example.duckdns.org domain name.
+ Create networks
  + `$ docker network create webproxy`
  + `$ docker network create ldap`
+ Reverse proxy a container
  + Connect container to proxy network
  + Environment variables needed to reverse proxy a container
    + VIRTUAL_HOST - e.g. VIRTUAL_HOST=service.example.duckdns.org
    + VIRTUAL_PORT - default 80 - e.g. VIRTUAL_PORT=8000
  + Adding letsencrypt
    + LETSENCRYPT_HOST - same as VIRTUAL_HOST - e.g. LETSENCRYPT_HOST=service.example.duckdns.org
    + LETSENCRYPT_EMAIL - your email to register with letsencrypt

## Services
[forward-sample] implements an example proxy to any remote web service that needs to be covered by the above system. e.g. a RPi running a remote service.

+ forward

[forward-sample]: ./
