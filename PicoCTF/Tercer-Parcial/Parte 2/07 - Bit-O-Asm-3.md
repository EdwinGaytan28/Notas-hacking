## Objetivo

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).
## Solucion
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt
--2024-05-06 21:51:23--  https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 461 [application/octet-stream]
Saving to: 'disassembler-dump0_c.txt'

disassembler-dump0_c.txt                                100%[===============================================================================================================================>]     461  --.-KB/s    in 0s      

2024-05-06 21:51:23 (213 MB/s) - 'disassembler-dump0_c.txt' saved [461/461]

edwin2809-picoctf@webshell:~$ cat disassembler-dump0_c.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4
<+29>:    mov    eax,DWORD PTR [rbp-0xc]
<+32>:    imul   eax,DWORD PTR [rbp-0x8]
<+36>:    add    eax,0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]
<+47>:    pop    rbp
<+48>:    ret
edwin2809-picoctf@webshell:~$ python
Python 3.10.12 (main, Nov 20 2023, 15:14:05) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int((0x9fe1a * 0x4) + 0x1f5))
2619997
Bandera 
picoCTF{2619997}
```
## Notas adicionales

## Referencias