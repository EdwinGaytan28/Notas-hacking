## Objetivo
#### Description

I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...Connect to the program on our server: `nc saturn.picoctf.net 65482`Download the program: [chal.py](https://artifacts.picoctf.net/c/297/chal.py)
## Solucion
```
edwin2809-picoctf@webshell:~$ nano exp.py 
edwin2809-picoctf@webshell:~$ python exp.py 
[+] Opening connection to saturn.picoctf.net on port 51475: Done
/home/edwin2809-picoctf/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/edwin2809-picoctf/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 35680258157434290983020734223580651160120649309751757044723280286576337848357
d= 44594269572789770571856807304895401377688669036621969172238169235729694320073
/home/edwin2809-picoctf/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  2922574644991923193967779580340929920089582302653093993640972897202016976654624200
[2, 2, 2, 5, 5, 7, 41, 43, 1373, 1619, 7457, 16097, 1369619, 142047233, 164279263793237200063, 138849235455517169402754247]
{319317793653065460577010219484993040691, 197935399991476362919768433698863077879, 305828462579022164838412629153648851687, 182772916580852856205665888216941362301, 284293907462278170526134037601137443971}
bMsEU86wK6Y4V8To
/home/edwin2809-picoctf/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> bMsEU86wK6Y4V8To\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_38268294}\r\n'
bMsEU86wK6Y4V8To
[*] Closed connection to saturn.picoctf.net port 51475
edwin2809-picoctf@webshell:~$ 
```

```
Codigo usado 
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
   # initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
       # Generating sub list
        comb += [list(j) for j in combinations(l, i)]
   # Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
  # this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 51475)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
  # multiply them together to get p-1
   for k in l:
      product = product * k
  # if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
     # decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
        # see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue
```
## Notas adicionales

## Referencias