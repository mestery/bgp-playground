# BGP Playground

A fun playground to learn about BGP with [ExaBGP](https://github.com/Exa-Networks/exabgp)
and [Quagga](https://www.quagga.net).

## To Use

Simply clone this repo and run the following:

```
$ docker-compose up -d
```

You can then look at the Quagga instance to see the BGP sessions:

```
$ docker exec -it quagga bash                                                                                                                                                                                                TSTP ✘  took 2m 54s    
root@7f524de8571c:~# telnet localhost 2605
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.

Hello, this is Quagga (version 1.1.1).
Copyright 1996-2005 Kunihiro Ishiguro, et al.


User Access Verification

Password:
quagga> show bgp sum
quagga> show bgp summary

IPv4 Unicast Summary:
---------------------
BGP router identifier 169.254.2.200, local AS number 65000
RIB entries 5, using 560 bytes of memory
Peers 3, using 27 KiB of memory

Neighbor        V         AS MsgRcvd MsgSent   TblVer  InQ OutQ Up/Down  State/PfxRcd
169.254.2.11    4 65045     263     267        0    0    0 00:21:53        0
169.254.3.12    4 67045     263     266        0    0    0 00:21:52        0
169.254.3.13    4 67046     263     266        0    0    0 00:21:53        0

Total number of neighbors 3

IPv4 Multicast Summary:
-----------------------
No IPv4 neighbor is configured

IPv4 VPN Summary:
-----------------
No IPv4 neighbor is configured

IPv4 Encap Summary:
-------------------
No IPv4 neighbor is configured

IPv6 Unicast Summary:
---------------------
No IPv6 neighbor is configured

IPv6 Multicast Summary:
-----------------------
No IPv6 neighbor is configured

IPv6 VPN Summary:
-----------------
No IPv6 neighbor is configured

IPv6 Encap Summary:
-------------------
No IPv6 neighbor is configured
quagga>
```
