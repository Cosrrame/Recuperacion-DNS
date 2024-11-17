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

















vagrant@dnsa:~$ nslookup 192.168.57.100 192.168.57.10
100.57.168.192.in-addr.arpa     name = server02.aulas.ies.test.

vagrant@dnsa:~$ nslookup 192.168.57.101 192.168.57.10
101.57.168.192.in-addr.arpa     name = pc04.aulas.ies.test.

vagrant@dnsa:~$ nslookup 192.168.57.102 192.168.57.10
102.57.168.192.in-addr.arpa     name = pc05.aulas.ies.test.

vagrant@dnsa:~$ nslookup 192.168.57.103 192.168.57.10
103.57.168.192.in-addr.arpa     name = pc06.aulas.ies.test.

vagrant@dnsa:~$ nslookup 192.168.57.104 192.168.57.10
104.57.168.192.in-addr.arpa     name = pc07.aulas.ies.test.

vagrant@dnsa:~$ dig -x 192.168.57.100 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.100 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 2667
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: eeaf28b76a2f97980100000067391fabe70359205b603e36 (good)
;; QUESTION SECTION:
;100.57.168.192.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
100.57.168.192.in-addr.arpa. 604800 IN  PTR     server02.aulas.ies.test.

;; Query time: 3 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:41:47 UTC 2024
;; MSG SIZE  rcvd: 121

vagrant@dnsa:~$ dig -x 192.168.57.101 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.101 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 29123
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: b5f386f58364b4730100000067391fb12ce07fe28e0cb763 (good)
;; QUESTION SECTION:
;101.57.168.192.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
101.57.168.192.in-addr.arpa. 604800 IN  PTR     pc04.aulas.ies.test.

;; Query time: 0 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:41:53 UTC 2024
;; MSG SIZE  rcvd: 117

vagrant@dnsa:~$ dig -x 192.168.57.102 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.102 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 32430
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: 10d86927f50f98c40100000067391fb486137fccc582da87 (good)
;; QUESTION SECTION:
;102.57.168.192.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
102.57.168.192.in-addr.arpa. 604800 IN  PTR     pc05.aulas.ies.test.

;; Query time: 4 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:41:56 UTC 2024
;; MSG SIZE  rcvd: 117

vagrant@dnsa:~$ dig -x 192.168.57.103 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.103 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 48180
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: 6714e172b0140a370100000067391fb787cdd94ef64a1743 (good)
;; QUESTION SECTION:
;103.57.168.192.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
103.57.168.192.in-addr.arpa. 604800 IN  PTR     pc06.aulas.ies.test.

;; Query time: 0 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:41:59 UTC 2024
;; MSG SIZE  rcvd: 117

vagrant@dnsa:~$ dig -x 192.168.57.104 @192.168.57.10

; <<>> DiG 9.18.28-1~deb12u2-Debian <<>> -x 192.168.57.104 @192.168.57.10
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 44219
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: 8a8783a58659bcac0100000067391fba35d2d41328372b6b (good)
;; QUESTION SECTION:
;104.57.168.192.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
104.57.168.192.in-addr.arpa. 604800 IN  PTR     pc07.aulas.ies.test.

;; Query time: 0 msec
;; SERVER: 192.168.57.10#53(192.168.57.10) (UDP)
;; WHEN: Sat Nov 16 22:42:02 UTC 2024
;; MSG SIZE  rcvd: 117

vagrant@dnsa:~$ host 192.168.57.100 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

100.57.168.192.in-addr.arpa domain name pointer server02.aulas.ies.test.
vagrant@dnsa:~$ host 192.168.57.101 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

101.57.168.192.in-addr.arpa domain name pointer pc04.aulas.ies.test.
vagrant@dnsa:~$ host 192.168.57.102 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

102.57.168.192.in-addr.arpa domain name pointer pc05.aulas.ies.test.
vagrant@dnsa:~$ host 192.168.57.103 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

103.57.168.192.in-addr.arpa domain name pointer pc06.aulas.ies.test.
vagrant@dnsa:~$ host 192.168.57.104 192.168.57.10
Using domain server:
Name: 192.168.57.10
Address: 192.168.57.10#53
Aliases:

104.57.168.192.in-addr.arpa domain name pointer pc07.aulas.ies.test.
vagrant@dnsa:~$




































