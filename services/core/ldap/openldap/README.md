# OpenLDAP

## Resources
+ https://www.openldap.org/
+ https://github.com/osixia/docker-openldap

## Guide

### PHP LDAP Admin

#### Login
Login DN: cn=admin,dc=example,dc=duckdns,dc=org
Password: LDAP_ADMIN_PASSWORD

### Setup
+ Creating child entries - click parent and then create child entry
  + organisationalUnit - use template
  + iNetOrgPerson - default, then find in list
  + groupOfNames - default, then find in list

+ Create 2 organisationalUnits (ou)
  + ou=users
    + iNetOrgPerson - set cn, sn, email and password (ssha)
  + ou=groups
    + groupOfNames
      + cn=admin,ou=groups
      + cn=user,ou=groups
