# 0x02-shell_redirections

## 0. Hello World

Write a script that prints “Hello, World”, followed by a new line to the standard output.

```bash
julien@ubuntu:/tmp/h$ ./0-hello_world 
Hello, World
julien@ubuntu:/tmp/h$ ./0-hello_world | cat -e
Hello, World$
julien@ubuntu:/tmp/h$ 
```

## 1. Confused smiley

Write a script that displays a confused smiley "(Ôo)'.

```bash
julien@ubuntu:/tmp/h$ ./1-confused_smiley 
\"(Ôo)\'
julien@ubuntu:/tmp/h$ 
```

## 2. Let's display a file

Display the content of the /etc/passwd file.

Example:

```bash
$ ./2-hellofile
##
# User Database
#
...
```
