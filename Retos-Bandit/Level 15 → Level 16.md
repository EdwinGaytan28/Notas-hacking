## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 17 11:57:28 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 17 11:57:28 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 17 11:56:28 2024 GMT; NotAfter: Feb 17 11:57:28 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEZKdJlDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjE3MTE1NjI4WhcNMjQwMjE3MTE1NzI4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDG
9Cqj59t9aXqZ/6Zbv88YMC5s3jyYN1tEiaWhdu+VD+z+o0L4nHKFcb92BRN9QG7q
92osLAnowzZPz4i+ZoEQ/3Xt6hbZuwOK2iL+p9X59sP/yrJUiiciQxZeyvnTUhT0
y9gbpMfIoAh/IjcMp7fDshItpA5lowi2JgVj31GVcEvEIbSGP/QdGchtccTEvrjC
OJ8IXyxyJt1Oy9CjRy/+N1c367/bu0Ww06W0nX0/hZP5+jVt+LECrlxBAIIXSr8g
ZyDjWVlguC3JtYSVnhhAOWSN9TaR1JDTfw191lBeBQsrqt8MSs3mB4U7F8UFbiq+
g69XER7kr9BG98tQIRFHAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQC6
fyai/YINkq3xU+3Uv1hQJxAFr+I1YrhKMOjlZGxeJoi9CqaLh8hS4uKgggzVlz1w
RizKiiDXLriXCh8af1x7knawPKnZf3lorVh/4hI/BKy6hzMQxf26EAOEU6qEyvub
x2viq7JBvEG3GVDSYB9BmYS/YXMn34WdG2ep8JqQEFh/7gphPZpDIeE6Ta3opi61
gm0UDF4HK5t4yxzrq4/X8vnH1u8w0tClZIDJoKfr2IwMXMRvvTDjtRqWK+XP1xvr
PrjwX2GINZbpu+xpXqShWNRlJ+6t2THoiQWhxPr9yFHtUOBfx3xB9naLD3Yy+bJ/
gp5JXeW5duZ6j2Q6YIRs
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: D4F6E53AA162FDD7288E93CD7DE56D515B5770D44149790794BCEEDC67608E39
    Session-ID-ctx:
    Resumption PSK: 63D813455A01EB92709DFD91D4EB262A969D0A6D2559ED7E19F7237CD5978FFC535FF52CC8D7B3570726C63C7FF35F10
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 08 08 72 41 b0 9d cc 8c-9b 2e 39 b7 e1 13 fd 6c   ..rA......9....l
    0010 - 47 4a 60 ef e6 4f 5e 44-54 26 e6 04 84 34 6b a4   GJ`..O^DT&...4k.
    0020 - 37 36 4d 38 1d 75 71 a1-4b 8f 83 91 00 7b ad e5   76M8.uq.K....{..
    0030 - be 61 1b d8 c2 a5 d5 9d-c8 3a df 6a 29 8c 2f db   .a.......:.j)./.
    0040 - ce 91 a8 6f 8f d3 60 ea-a0 1b f2 3d 85 4a a0 e9   ...o..`....=.J..
    0050 - b1 fc 67 bd 04 9c d4 24-f4 01 8a 7a a8 36 85 5a   ..g....$...z.6.Z
    0060 - 68 7e e9 de a4 28 3b d8-6c c9 a2 d2 f6 a0 98 3b   h~...(;.l......;
    0070 - d8 81 73 aa 1e 03 39 1e-ba 07 1f 4c dd 2f 45 79   ..s...9....L./Ey
    0080 - 57 a7 08 a4 2e f2 bd d1-62 51 44 c5 9b 0c 3c 08   W.......bQD...<.
    0090 - 23 6b 5a aa a2 d5 ff d6-cd 79 99 fa cf af 31 0c   #kZ......y....1.
    00a0 - b2 04 04 f4 67 f0 5d 78-9d 91 1d 31 70 69 26 f5   ....g.]x...1pi&.
    00b0 - c0 b8 90 15 ff c7 f2 2b-fc 18 bd 5b c9 0f 01 ad   .......+...[....
    00c0 - e4 99 25 d5 c0 58 21 61-e8 8e bc 5f ed 29 48 6e   ..%..X!a..._.)Hn

    Start Time: 1708233714
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 62BEBD5160CFA9D2F170234CE5EEF0B57E5A5592B20CE68A88165541B7079270
    Session-ID-ctx:
    Resumption PSK: E54A87480DE80F8617A13934D582E4ECC06B49760ED849D7C769E9AA853C182510AAE494E41F7D921BAE373EE17AB514
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 08 08 72 41 b0 9d cc 8c-9b 2e 39 b7 e1 13 fd 6c   ..rA......9....l
    0010 - 34 27 b2 7c ae e9 10 c0-fa d8 47 23 7a cd 6a 77   4'.|......G#z.jw
    0020 - cf d1 40 36 08 0b 89 52-e5 0c 29 76 de ce 88 2f   ..@6...R..)v.../
    0030 - 6d c6 c5 e9 6e 0c 4e 74-9d 1a 9f f4 91 84 ec d1   m...n.Nt........
    0040 - 39 8d ea f2 23 0e fe b9-e3 36 06 a1 41 ce ed bc   9...#....6..A...
    0050 - 0b 7e 27 ec 89 3f 34 18-74 4d df a4 e3 14 35 e7   .~'..?4.tM....5.
    0060 - 08 4d 0d 42 ed ba 50 91-4b 76 b5 ab 8c 97 8e 56   .M.B..P.Kv.....V
    0070 - 5e 01 6c 3f 24 ac ca 22-cf c5 bb 16 32 f1 ba 27   ^.l?$.."....2..'
    0080 - 5d b6 ed 0a ce 3a 42 72-1c f4 93 20 36 1d 70 c6   ]....:Br... 6.p.
    0090 - 57 29 4d 0d aa 04 d9 b9-32 8f e3 dd d1 d5 33 e2   W)M.....2.....3.
    00a0 - 59 6c 62 88 97 66 0d 81-1d 48 70 e3 2d 40 c3 da   Ylb..f...Hp.-@..
    00b0 - ec 7d c3 f1 aa f8 b4 d9-0c 7f 76 9b 2f d3 9e 23   .}........v./..#
    00c0 - c8 1a 0d 90 ae 18 01 0e-25 9f e9 90 47 50 9b 67   ........%...GP.g

    Start Time: 1708233714
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```
## Notas adicionales

## Referencias