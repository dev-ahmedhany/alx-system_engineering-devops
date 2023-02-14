# 0x03. Shell, init files, variables and expansions

## 0. \<o>

Create a script that creates an alias.

Name: ls
Value: rm *

```bash
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 
```

> answer

```bash
alias <name>='<value>'
```

```bash
#!/bin/bash
alias ls='rm *'
```

## 1. Hello you

Create a script that prints hello user, where user is the current Linux user.

```bash
julien@ubuntu:/tmp/0x03$ id
uid=1000(julien) gid=1000(julien) groups=1000(julien),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)
julien@ubuntu:/tmp/0x03$ ./1-hello_you 
hello julien
julien@ubuntu:/tmp/0x03$ 
```

> answer

```bash
echo "hello $USER"
```

> wrong answers :

```bash
echo "hello $(whoami)"
```

```bash
[Got]
hello root

(11 chars long)

[Expected]
hello MyUser

(13 chars long)
```
