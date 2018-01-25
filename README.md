## dnsmasq with regex and extended cache limit

Version: 2.78

Inspired by these repos:
- [dnsmasq-regexp_2.76](https://github.com/spacedingo/dnsmasq-regexp_2.76)
- [dnsmasq-regexp_2.78](https://github.com/spacedingo/dnsmasq-regexp_2.78)
- [dnsmasq-regex](https://github.com/cuckoohello/dnsmasq-regex)

Original regex patch for dnsmasq 2.63
- [using regular expressions in server list](http://lists.thekelleys.org.uk/pipermail/dnsmasq-discuss/2013q2/007124.html)
- [dnsmasq-2.63-regex.patch](http://lists.thekelleys.org.uk/pipermail/dnsmasq-discuss/attachments/20130428/b3fc0de0/attachment.obj)

Offical dnsmasq:
- [dnsmasq](http://www.thekelleys.org.uk/dnsmasq/)

## Compile

For Debian/ubuntu:

```
sudo apt install libpcre3-dev

git clone https://github.com/lixingcong/dnsmasq-regex

cd dnsmasq-regex

make
```

## Config file example

```
server=/:.*google.*:/8.8.8.8#53
server=/:.*facebook.*:/8.8.8.8#53

no-reslov
no-poll

cache-size=100000
```