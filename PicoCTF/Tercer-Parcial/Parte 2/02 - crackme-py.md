## Objetivo

crackme.py
## Solucion
```
A:4@r%uL`M-^M0c0AbcM-MFE07b34c`_6N
Usamos el siguiente codigo 
def rot47(string):
    enc_dec = ''
    for char in string:
        ascii_code = ord(char)
        if 33 <= ascii_code <= 79:
            enc_dec += chr(ascii_code + 47)
        elif 80 <= ascii_code <= 126:
            enc_dec += chr(ascii_code - 47)
        else:
            enc_dec += char
    return enc_dec

if __name__ == '__main__':
    print(rot47(input('Enter string: ')))
    
Bandera 
picoCTF{1|\/|_4_p34|\|ut_f3bc410e}
```
## Notas adicionales

## Referencias