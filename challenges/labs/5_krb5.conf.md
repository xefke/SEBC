```
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = XEFKE.PA
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 udp_preference_limit = 1

[realms]
 XEFKE.PA = {
  kdc = node102.sebc
  admin_server = node102.sebc
 }

[domain_realm]
 .sebc = XEFKE.PA
 sebc = XEFKE.PA
```