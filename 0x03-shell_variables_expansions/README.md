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

### answer

```bash
alias <name>='<value>'
```

```bash
#!/bin/bash
alias ls='rm *'
```
