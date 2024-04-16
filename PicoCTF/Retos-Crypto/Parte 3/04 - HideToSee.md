## Objetivo
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/236/atbash.jpg).

## Solución
```
──(kali㉿kali)-[~]
└─$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                             
┌──(kali㉿kali)-[~]
└─$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_zx751vx6}

picoCTF{atbash_crack_ac751ec6}
```
## Notas adicionales

## Referencias