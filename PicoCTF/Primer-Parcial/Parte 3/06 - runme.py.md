## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2024-03-03 23:30:28--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                                100%[===============================================================================================================================>]     270  --.-KB/s    in 0s      

2024-03-03 23:30:28 (4.22 MB/s) - 'runme.py' saved [270/270]

edwin2809-picoctf@webshell:~$ python3 runme.py 
picoCTF{run_s4n1ty_run}
edwin2809-picoctf@webshell:~$ ^C
```
## Notas adicionales

## Referencias

