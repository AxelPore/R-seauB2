# TP2B2 Réseau




## I. Topologie réseau


```
[aku2@localhost ~]$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:cc:f3:8f brd ff:ff:ff:ff:ff:ff
    inet 10.1.1.11/24 brd 10.1.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fecc:f38f/64 scope link
       valid_lft forever preferred_lft forever
```

```
[aku2@localhost ~]$ ip r s
default via 10.1.1.254 dev enp0s3 proto static metric 100
10.1.1.0/24 dev enp0s3 proto kernel scope link src 10.1.1.11 metric 100
10.1.2.0/24 via 10.1.1.254 dev enp0s3 proto static metric 100
```
```
[aku2@localhost ~]$ ping 10.1.2.12
PING 10.1.2.12 (10.1.2.12) 56(84) bytes of data.
64 bytes from 10.1.2.12: icmp_seq=1 ttl=63 time=0.831 ms
64 bytes from 10.1.2.12: icmp_seq=2 ttl=63 time=0.992 ms
64 bytes from 10.1.2.12: icmp_seq=3 ttl=63 time=0.985 ms
64 bytes from 10.1.2.12: icmp_seq=4 ttl=63 time=0.918 ms
64 bytes from 10.1.2.12: icmp_seq=5 ttl=63 time=0.427 ms
^C
--- 10.1.2.12 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4038ms
rtt min/avg/max/mdev = 0.427/0.830/0.992/0.209 ms
```
```
[aku2@localhost ~]$ traceroute 10.1.2.12
traceroute to 10.1.2.12 (10.1.2.12), 30 hops max, 60 byte packets
 1  _gateway (10.1.1.254)  0.534 ms  0.501 ms  0.492 ms
 2  10.1.2.12 (10.1.2.12)  1.085 ms !X  1.395 ms !X  1.385 ms !X
```