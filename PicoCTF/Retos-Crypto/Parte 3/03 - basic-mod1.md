## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/129/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
```
datos = open('message.txt').read().split()

flag = ''

for n in datos:
	c = int(n) % 37
	if c>=0 and c<=25:
		s = chr(c+65)
	elif c >= 26 and c <= 35:
		s = chr(c+22)
	else:
		s = '_'
	flag += s
print(f"picoCTF{{{flag}}}")
```


```
──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/129/message.txt
--2024-04-16 14:29:00--  https://artifacts.picoctf.net/c/129/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 86 [application/octet-stream]
Saving to: ‘message.txt’

message.txt         100%[================>]      86  --.-KB/s    in 0s      

2024-04-16 14:29:08 (108 MB/s) - ‘message.txt’ saved [86/86]

                                                                             
┌──(kali㉿kali)-[~]
└─$ cat message.txt 
350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213                                                                              
┌──(kali㉿kali)-[~]
└─$ python3 reto2.py  
picoCTF{R0UND_N_R0UND_ADD17EC2}

```
## Notas adicionales

## Referencias