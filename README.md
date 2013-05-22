# ssh
My personal secure sshd configuration.
## Adding a user to the configuration
### RSA
```shell
adduser [username]
chmod 770 /home/[username]
su [username]
cd
ssh-keygen -t rsa 4096
chmod 600 .ssh/id_dsa.pub
```
### DSA
```shell
adduser [username]
chmod 770 /home/[username]
su [username]
cd
ssh-keygen -t dsa
chmod 600 .ssh/id_dsa.pub
```