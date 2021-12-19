# locate-find
Comparing locate and find


## Using Locate

```bash

#install it
sudo yum install mlocate

#update it
sudo updatedb

#use it
locate .zshrc

#count
locate -c .zshrc

#case insensitive
locate -i .ZSHRC
```

## Using Find

find . -name .zshrc

### Much slower than locate

```bash
[cloudshell-user@ip-10-0-100-158 ~]$ time sudo find / -name .zshrc
/home/cloudshell-user/.zshrc
/etc/skel/.zshrc

real    0m0.352s
user    0m0.146s
sys     0m0.199s


[cloudshell-user@ip-10-0-100-158 ~]$ time locate .zshrc
/etc/skel/.zshrc
/home/cloudshell-user/.zshrc
/home/cloudshell-user/other/.zshrc

real    0m0.035s
user    0m0.035s
sys     0m0.000s
```
