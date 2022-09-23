# omikhaylov_infra
omikhaylov Infra repository

## Задание №3
```
root@debian-10-x86-64:~# cat .ssh/config
Host someinternalhost
    HostName 10.128.0.32
    ProxyCommand ssh -W %h:%p bastion
    User appuser
    IdentityFIle ~/.ssh/id_rsa_2
Host bastion
    HostName 51.250.10.79
    User appuser
    IdentityFIle ~/.ssh/id_rsa
root@debian-10-x86-64:~# ssh someinternalhost
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 5.4.0-124-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
Failed to connect to https://changelogs.ubuntu.com/meta-release-lts. Check your Internet connection or proxy settings

Last login: Fri Sep 23 13:29:26 2022 from 10.128.0.31
appuser@someinternalhost:~$
```
