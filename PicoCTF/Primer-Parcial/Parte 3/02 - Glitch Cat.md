## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 52682`
## Solución
```
edwin2809-picoctf@webshell:~$ nc saturn.picoctf.net 52682
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
^C
edwin2809-picoctf@webshell:~$ 
El valor ASCII de la cadena resultante de concatenar los caracteres es: bda68f75.
```
## Notas adicionales

## Referencias

