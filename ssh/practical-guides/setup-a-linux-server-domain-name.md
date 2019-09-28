# Setup A Linux Server Domain Name

## Learning Outcomes 

* Understand IP addresses map to domain names 

`hostname` command shows your server’s hostname. `hostname -f` shows your FQDN. `dnsdomainname` command shows your domain name of server!



Nameservers are your DNS servers and are not what points to you.  The DNS servers hold entries that point to you.   


Steps in setting up a domain...

1. Register it \(you've done this\)

2. Point the registration to your DNS host \(I use CloudFlare\) which should never be your registrar

3. In DNS point the domain name you want to the IP that you want.

FQDN

DHCP

#### Domain Registry Google 

#### [https://lookup.icann.org/lookup](https://lookup.icann.org/lookup) Cloudflare nameserver

Becoming a super hero is a fairly straight forward process:

```
$ give me super-powers
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

```
// Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



