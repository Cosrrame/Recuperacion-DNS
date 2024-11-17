vagrant@dnsa:~$ nslookup 192.168.57.10 192.168.57.10
10.57.168.192.in-addr.arpa      name = server01.informatica.ies.test.
10.57.168.192.in-addr.arpa      name = dnsa.ies.test.

vagrant@dnsa:~$ dig -x 192.168.57.10 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.10 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 22147
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: 53222e70f369cdda0100000067391c8704f7d4d60b1f693d (good)
;; QUESTION SECTION:
;10.57.168.192.in-addr.arpa.    IN      PTR

;; ANSWER SECTION:
10.57.168.192.in-addr.arpa. 604800 IN   PTR     server01.informatica.ies.test.
10.57.168.192.in-addr.arpa. 604800 IN   PTR     dnsa.ies.test.

;; Query time: 3 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:28:23 UTC 2024
;; MSG SIZE  rcvd: 153

vagrant@dnsa:~$ host 192.168.57.10 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

10.57.168.192.in-addr.arpa domain name pointer dnsa.ies.test.
10.57.168.192.in-addr.arpa domain name pointer server01.informatica.ies.test.