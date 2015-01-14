# OpenSSH Configuration
Personal OpenSSH configuration template, you may use it as a start point to create your own.

## Install
Clone the repository or just download the `sshd.conf` file to the target computer, edit it to meet your preferences and
copy/move it to `/etc/ssh/sshd_conf`. Reload the OpenSSH daemon to apply the new configuration. But be careful, since a
wrong configuration may make it impossible for you to connect to the computer, in case you only have remote access.

## New User
In order to create a new user with a key for authentication use the following commands (of course you have to exchange
`fleshgrinder` with the name of your user):

```shell
adduser fleshgrinder
chmod 770 /home/fleshgrinder
su - fleshgrinder
cd
ssh-keygen -t rsa -b 4096
chmod 600 .ssh/id_dsa.pub
```

## License
> This is free and unencumbered software released into the public domain.
>
> For more information, please refer to <http://unlicense.org>
