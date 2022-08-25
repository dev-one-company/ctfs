# Welcome CTF

ip: 10.0.0.10

## Search dir

/admin
/admin/index.php
/admin/phpinfo.php
/login.php


## Answers

- Primeiro informe qual sistema operacional está rodando nessa máquina. 5 pontos
on `/admin/phpinfo.php` has the OS

- Agora queremos que você informe qual webserver e sua versão está rodando nesse servidor. 10 pontos
access any not found route to get the flag

- Informe também qual PHP e versão está rodando nesse servidor. 15 pontos
on `/admin/phpinfo.php` has the type and version

- Agora explore a falha que o admin deixou na aplicação web. 20 pontos
on /admin/index.php page create a cookie called `user` and set to `admin`
then you get the flag or you can execute my exploit on `./exploits/index.js`

```bash
node exploits/index.js
```
