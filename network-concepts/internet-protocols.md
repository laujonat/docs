# Internet Protocols

## Protocols



### IPv4



### IPv6

IPv6 addresses have two logical parts:a 64-bit network prefix, and a 64-bit host address part. \(The host address is often automatically generated from the interface MAC address.\[37\]\) An IPv6 address is represented by 8 groups of 16-bit hexadecimal values separated by colons \(:\) shown as follows:



`ipv6() {   
   i = ifconfig en0 | grep inet6   
   echo $i | awk -F " " '{print $2}' | sed 's/%en0//'   
}`



[https://www.justinrummel.com/working-with-ipv6-and-mac-os-x/](https://www.justinrummel.com/working-with-ipv6-and-mac-os-x/)

{% embed url="http://www.steves-internet-guide.com/ipv6-guide/" %}

[https://www.techrepublic.com/blog/data-center/breaking-down-an-ipv6-address-what-it-all-means/](https://www.techrepublic.com/blog/data-center/breaking-down-an-ipv6-address-what-it-all-means/)

