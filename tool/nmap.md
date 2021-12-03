## nmap
假設攻擊者要攻擊區域網路內的被攻擊者，需要查詢到被攻擊者的ip位置，則可以使用nmap
## test
### Attacker
```linux
# yum install nmap
# nmap -sP 192.168.56.0/24 //搜索區網內其他的ip
```

```
Starting Nmap 6.40 ( http://nmap.org ) at 2021-12-02 15:39 CST
Nmap scan report for 192.168.56.1
Host is up (0.00045s latency).
MAC Address: 0A:00:27:00:00:0C (Unknown)
Nmap scan report for 192.168.56.100
Host is up (0.00019s latency).
MAC Address: 08:00:27:C1:AC:EA (Cadmus Computer Systems)
Nmap scan report for 192.168.56.105
Host is up (0.00019s latency).
MAC Address: 08:00:27:82:88:10 (Cadmus Computer Systems)
Nmap scan report for 192.168.56.103
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 2.15 seconds
```

```linux
# ip route show
# ping 192.168.56.100 //測試
# ping 192.168.56.103 //測試
# nmap -A 192.168.56.105 //觀看詳細資訊
```

```
Starting Nmap 6.40 ( http://nmap.org ) at 2021-12-02 15:49 CST
Nmap scan report for 192.168.56.105
Host is up (0.00041s latency).
Not shown: 999 filtered ports
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.4 (protocol 2.0)
| ssh-hostkey: 2048 c4:0d:fd:1d:90:4a:25:56:19:c5:89:db:dc:d9:31:b2 (RSA)
|_256 f5:65:f8:1c:c2:9a:8e:6b:22:a4:06:bb:22:b7:49:4e (ECDSA)
MAC Address: 08:00:27:82:88:10 (Cadmus Computer Systems)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Linux 2.6.32 - 3.6 (93%), Linux 2.6.32 - 3.9 (93%), Linux 3.0 - 3.9 (93%), Linux 2.6.22 - 2.6.36 (90%), Linux 2.6.39 (90%), Linux 2.6.32 (90%), Crestron XPanel control system (89%), Netgear DG834G WAP or Western Digital WD TV media player (89%), Linux 2.6.32 - 2.6.35 (88%), Linux 2.6.32 - 3.2 (88%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 1 hop

TRACEROUTE
HOP RTT     ADDRESS
1   0.41 ms 192.168.56.105

OS and Service detection performed. Please report any incorrect results at http://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 11.99 seconds
[root@skycentos user]# ^C
[root@skycentos user]# ^C
[root@skycentos user]# ^C
[root@skycentos user]# nmap -A 192.168.56.105

Starting Nmap 6.40 ( http://nmap.org ) at 2021-12-02 15:55 CST
Nmap scan report for 192.168.56.105
Host is up (0.00042s latency).
Not shown: 999 filtered ports
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.4 (protocol 2.0)
| ssh-hostkey: 2048 c4:0d:fd:1d:90:4a:25:56:19:c5:89:db:dc:d9:31:b2 (RSA)
|_256 f5:65:f8:1c:c2:9a:8e:6b:22:a4:06:bb:22:b7:49:4e (ECDSA)
MAC Address: 08:00:27:82:88:10 (Cadmus Computer Systems)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Linux 2.6.32 - 3.9 (93%), Linux 3.0 - 3.9 (93%), Linux 2.6.32 - 3.6 (92%), Linux 2.6.32 (90%), Linux 2.6.22 - 2.6.36 (90%), Linux 2.6.39 (90%), Crestron XPanel control system (89%), Netgear DG834G WAP or Western Digital WD TV media player (89%), Linux 3.3 (89%), Linux 2.6.32 - 2.6.35 (88%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 1 hop

TRACEROUTE
HOP RTT     ADDRESS
1   0.42 ms 192.168.56.105

OS and Service detection performed. Please report any incorrect results at http://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.40 seconds

```
