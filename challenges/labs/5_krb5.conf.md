```
[libdefaults]
default_realm = MAJIMENEZ.CO.UK 
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = rc4-hmac arcfour-hmac
default_tkt_enctypes = rc4-hmac arcfour-hmac
permitted_enctypes = rc4-hmac arcfour-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
MAJIMENEZ.CO.UK  = {
kdc = ip-172-31-37-252
admin_server = ip-172-31-37-252
}
```
**MFE**: I'd guess you're allowing Cloudera Manager to write the file for you. The field organization discourages this practice for a couple of reasons. Feel free to inquire if you're curious.
