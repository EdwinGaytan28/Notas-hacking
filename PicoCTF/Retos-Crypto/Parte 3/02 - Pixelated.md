## Objetivo

## Solución
```
┌──(kali㉿kali)-[~]
└─$ convert scrambled1.png scrambled2.png +append flag8.png
                                                                             
┌──(kali㉿kali)-[~]
└─$ open flag8.png 
                                                                             
┌──(kali㉿kali)-[~]
└─$ convert scrambled1.png scrambled2.png -compose  flag9.png
convert-im6.q16: unrecognized compose operator `flag9.png' @ error/convert.c/ConvertImageCommand/1072.
                                                                             
┌──(kali㉿kali)-[~]
└─$ convert scrambled1.png scrambled2.png -compose add -composite flag.png
                                                                             
┌──(kali㉿kali)-[~]
└─$ open flag.png           

picoCTF{d72ea4af}
```
## Notas adicionales

## Referencias