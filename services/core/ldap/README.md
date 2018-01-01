## LDAP
LDAP is an protocol to a access and maintain distributed directory information services

### Requirements
`$ docker network create ldap`

### Consumers
+ base/authelia
+ other/nextcloud

### Providers

Implemented:
+ [OpenLDAP]

Wish:
+ [FreeIPA]

[OpenLDAP]: ./openldap
[FreeIPA]: https://www.freeipa.org
