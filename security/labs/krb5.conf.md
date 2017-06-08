<pre>
[libdefaults]
default_realm = MAJIMENEZ.ES
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
MAJIMENEZ.ES = {
kdc = ip-172-31-2-87
admin_server = ip-172-31-2-87
}
</pre>