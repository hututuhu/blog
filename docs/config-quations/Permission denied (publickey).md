文问题：
xxx@gerrit.com:Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

解决：
1、在.ssh文件夹下创建config文件，没用后缀名
2、往config文件里配置
```
# GERRIT
Host gerrit仓库域名
  HostName errit仓库域名
   PubkeyAcceptedKeyTypes +ssh-rsa
   User  gerrit用户名
   PreferredAuthentications publickey
   IdentityFile ~/.ssh/id_rsa
  Port 29418

```