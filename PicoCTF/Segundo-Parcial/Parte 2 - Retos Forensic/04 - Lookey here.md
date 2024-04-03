## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/125/anthem.flag.txt).
## Solucion
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/125/anthem.flag.txt
--2024-04-03 23:20:33--  https://artifacts.picoctf.net/c/125/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: 'anthem.flag.txt'

anthem.flag.txt                                        100%[==========================================================================================================================>] 106.12K  --.-KB/s    in 0.004s  

2024-04-03 23:20:33 (27.8 MB/s) - 'anthem.flag.txt' saved [108668/108668]

edwin2809-picoctf@webshell:~$ cat anthem.flag.txt | grep pico
      we think that the men of picoCTF{gr3p_15_@w3s0m3_58f5c024}
edwin2809-picoctf@webshell:~$ 



picoCTF{gr3p_15_@w3s0m3_58f5c024}
```
## Notas adicionales

## Referencias