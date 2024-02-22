## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solución
```
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2024-02-22 18:17 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0015s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.19 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 22 18:04:08 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 22 18:04:08 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 22 18:03:08 2024 GMT; NotAfter: Feb 22 18:04:08 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEWdQAXzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIyMTgwMzA4WhcNMjQwMjIyMTgwNDA4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC0
EWB28TWVpVUtrYSaYvmbjtrgpiTuEqg01/SReTOErvDgCyz8mhJ06BhcWK0RDiNz
E1BeQ1s7bo4V8knTeqgTd3cA9XIKO8BgqmGwYiPJyBVDMO+9S4dojnuJGViyhoM7
e0kKwdp7+uEER22koJg+ZqyI/dSSmvaDqMAU+D6FKxcxKjF8vTQzn0CLsYSXPHxT
mhshEAC8jWhYggcUxG0L1qMJnh/NL18e0jwBeCrE2PwsRuh1Qc6vl4Fd/mUByDJb
KSjsR3zDoegCWzh5lTAbnt5eaT47PBNA4foRLypdCG1tG+Cbgk6d0BGtluAJz9D8
5vEfrVpm38OelPOo0vBJAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAl
z9TnfQ4cqpUeKMFRzhzuHEvuglEdfmmWmhpQ+NnpcI686OZDshzpHFRVUQjwMulr
XuhDoohLwnd+AOB4BqYWWYoF2z1mo3rsxZxxCoI7y8SP331O46Aqc4SyKMEfYBXq
mCaK5VQebSZotRPqI6jS2W7/+UmJXXKG4pEKI5pBA5tTnvNSbh6Yk87cFlAitTcN
36V1lq8S7tj2BZSfcC+nyoqwPPeLTb5beQTmKG0/JFDnYeHCbVQALq5AhXXH5G67
ytpppb4itSOMr9bfv+Awx6PPLbOJ/gxF1c1HkXX5/Pjbdy2W4sCykvXAJBir2BFe
ixo6bdA2sW0cz3uzk5x7
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
    Session-ID: 2FCC037DEAADDF0F3F9BC18A1B90C1401B116038B85E327E63531AD31BA4D782
    Session-ID-ctx:
    Resumption PSK: 28AAE7661283A49F52AF30B9FC9BAA4AB3AEAF1D6DAD8EE4D323353959F3D3C57B7A75CD18E7888B602B8875D00ACBEB
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - d5 fe 56 7f 7c 44 0f 09-aa 20 5d ad 9d 9b 72 2f   ..V.|D... ]...r/
    0010 - 1d 66 30 96 96 75 e6 08-44 77 d2 66 4f 23 f9 77   .f0..u..Dw.fO#.w
    0020 - 20 8a e2 d3 dd ed 68 56-98 3e e5 30 8a ae e7 45    .....hV.>.0...E
    0030 - a3 3e 1c 2c 7e 90 45 21-69 43 cc 1c af 67 20 a9   .>.,~.E!iC...g .
    0040 - 63 40 73 73 39 d2 b1 36-b6 af 78 e3 b0 36 aa 40   c@ss9..6..x..6.@
    0050 - 54 7d e2 19 25 2b d0 ce-48 c5 6d d7 a6 08 8c 75   T}..%+..H.m....u
    0060 - f1 d3 e4 f1 78 47 62 bb-ed 2d a6 54 94 1f 85 64   ....xGb..-.T...d
    0070 - 21 12 16 9e 81 26 5a cd-7c 41 7e 64 df fa 96 64   !....&Z.|A~d...d
    0080 - 59 14 e2 48 5b b2 e5 66-b0 d2 f1 0d 11 89 bd 8a   Y..H[..f........
    0090 - e4 3e c7 ea 5b bb b1 d6-3f 95 bf 8b 19 88 f6 fb   .>..[...?.......
    00a0 - 1e 7f 1e 86 b3 52 b1 5c-4a 7e 69 25 e0 77 68 33   .....R.\J~i%.wh3
    00b0 - a2 c5 23 49 1d 39 46 31-01 34 a9 23 c3 a2 ee 17   ..#I.9F1.4.#....
    00c0 - 92 f4 16 eb 01 49 2f 25-81 05 ae 91 b5 ba 77 1f   .....I/%......w.

    Start Time: 1708626000
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
    Session-ID: 1969CAF84126E3AC0298B680F0D5CE6734E7E4C72E39AFD62A88B1689015AC91
    Session-ID-ctx:
    Resumption PSK: B79D9A7CA6CA50EB64170D28A5793518C063523E0F40ECF10B13C8A2CA3F7A0BA15459F47F19699319EDCD7DC855C947
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - d5 fe 56 7f 7c 44 0f 09-aa 20 5d ad 9d 9b 72 2f   ..V.|D... ]...r/
    0010 - 08 07 38 ea 40 38 64 b8-c0 dd 9c f7 67 0d db e1   ..8.@8d.....g...
    0020 - 09 f3 d3 06 a2 97 0d 87-bd 5e 7b 03 b0 f1 21 6c   .........^{...!l
    0030 - 93 22 48 fc f2 76 61 63-a7 2a a9 7c 4c 51 52 76   ."H..vac.*.|LQRv
    0040 - ae 20 88 bc 81 d8 fe f8-50 16 eb a6 58 ef e6 9c   . ......P...X...
    0050 - e4 8e b8 22 df b3 29 1c-05 0c ac ae 15 17 48 2a   ..."..).......H*
    0060 - 50 c8 3c b8 f3 b4 ef 2e-fe 79 32 20 04 fa 02 8c   P.<......y2 ....
    0070 - 73 0b 07 54 ab aa ce af-29 ff 31 89 30 2f 7f 33   s..T....).1.0/.3
    0080 - 4b 80 53 fd 45 87 8d 8a-da f5 88 1c 1f 02 d6 bc   K.S.E...........
    0090 - 10 d1 68 49 e3 34 53 e1-b7 d4 31 ad db 7a 32 62   ..hI.4S...1..z2b
    00a0 - aa 38 8f 94 29 ec c1 ed-10 8a c4 cf a1 92 3f 0e   .8..).........?.
    00b0 - c2 28 42 8f 22 56 a5 f9-f1 63 b5 d9 a6 95 eb 89   .(B."V...c......
    00c0 - f7 07 60 b7 fa 55 24 b8-be aa da 1a e9 4b e7 6d   ..`..U$......K.m

    Start Time: 1708626000
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

C:\Users\edwin>notepad llave.txt

C:\Users\edwin>type llave.txt
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```
```
C:\Users\edwin>ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```
## Notas adicionales

## Referencias