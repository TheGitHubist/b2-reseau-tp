# Compte rendu

```powershell
[yasei@localhost ~]$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:62:84:65 brd ff:ff:ff:ff:ff:ff
    inet 10.1.1.11/24 brd 10.1.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fe62:8465/64 scope link
       valid_lft forever preferred_lft forever
[yasei@localhost ~]$ ip route show
default via 10.1.1.254 dev enp0s3 proto static metric 100
10.1.1.0/24 dev enp0s3 proto kernel scope link src 10.1.1.11 metric 100
10.1.2.0/24 via 10.1.1.254 dev enp0s3 proto static metric 100
[yasei@localhost ~]$ ping 10.1.2.12
PING 10.1.2.12 (10.1.2.12) 56(84) bytes of data.
64 bytes from 10.1.2.12: icmp_seq=1 ttl=63 time=0.613 ms
64 bytes from 10.1.2.12: icmp_seq=2 ttl=63 time=0.565 ms
64 bytes from 10.1.2.12: icmp_seq=3 ttl=63 time=0.548 ms
64 bytes from 10.1.2.12: icmp_seq=4 ttl=63 time=0.501 ms
64 bytes from 10.1.2.12: icmp_seq=5 ttl=63 time=0.747 ms
^C
--- 10.1.2.12 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4078ms
rtt min/avg/max/mdev = 0.501/0.594/0.747/0.084 ms
[yasei@localhost ~]$ traceroute 10.1.2.12
traceroute to 10.1.2.12 (10.1.2.12), 30 hops max, 60 byte packets
 1  _gateway (10.1.1.254)  0.822 ms  0.786 ms  0.771 ms
 2  10.1.2.12 (10.1.2.12)  0.605 ms !X  0.588 ms !X  0.508 ms !X
```

```powershell
[yasei@localhost ~]$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:c6:2f:e8 brd ff:ff:ff:ff:ff:ff
    inet 10.1.1.254/24 brd 10.1.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fec6:2fe8/64 scope link
       valid_lft forever preferred_lft forever
3: enp0s8: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:a2:61:d0 brd ff:ff:ff:ff:ff:ff
    inet 10.1.2.254/24 brd 10.1.2.255 scope global noprefixroute enp0s8
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fea2:61d0/64 scope link
       valid_lft forever preferred_lft forever
4: enp0s9: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:e8:81:ee brd ff:ff:ff:ff:ff:ff
    inet 10.0.4.15/24 brd 10.0.4.255 scope global dynamic noprefixroute enp0s9
       valid_lft 85297sec preferred_lft 85297sec
    inet6 fe80::329b:1b1e:b664:2d83/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
[yasei@localhost ~]$ ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=113 time=19.9 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=113 time=20.1 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=113 time=20.5 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=113 time=19.8 ms
```