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

## 2. The path to success is to take massive, determined action

Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.

```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path 
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action
julien@ubuntu:/tmp/0x03$ 
```

> answer

```bash
export PATH="$PATH:/action"
```

> wrong answers :

```bash
export PATH='$PATH:/action'
```

## 3. If the path be beautiful, let us not ask where it leads

Create a script that counts the number of directories in the PATH.

```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ . ./3-paths 
11
julien@ubuntu:/tmp/0x03$ PATH=/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:::::/hello
julien@ubuntu:/tmp/0x03$ . ./3-paths 
12
julien@ubuntu:/tmp/0x03$ 
```

> answer

```bash
echo $((`echo $PATH | grep -o ":/" | wc -l`+ 1))
```

> wrong answers :

```bash
echo $PATH | tr ':' '\n' | wc -l
```
