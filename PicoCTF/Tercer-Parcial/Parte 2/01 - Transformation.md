## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/a757282979af14ab5ed74f0ed5e2ca95/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solucion
```
Creamos un archivo .py con el siguiente codigo 
encoded_flag = open("enc").read()
flag = ""
for i in range(0, len(encoded_flag)):
    character1 = chr((ord(encoded_flag[i]) >> 8))
    character2 = chr(encoded_flag[i].encode('utf-16be')[-1])
    flag += character1
    flag += character2

print("Flag: " + flag)
Bandera
picoCTF{16_bits_inst34d_of_8_d52c6b93}
```
## Notas adicionales

## Referencias