# OpenSSH Configuration
Personal OpenSSH configuration template, you may use it as a start point to create your own.

```sh
rm -rf /etc/ssh
git clone https://github.com/Fleshgrinder/openssh-configuration.git /etc/ssh
cd /etc/ssh
./gen-moduli
./gen-host-keys
./create-group
./create-user fleshgrinder
service ssh restart                 # Debian / Ubuntu
service sshd restart                # CentOS / RHEL / Fedora / Redhat
/etc/rc.d/sshd restart              # FreeBSD
kill -HUP `cat /var/run/sshd.pid`   # UNIX
```

## Weblinks
- stribika: [Secure Secure Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html)

## License
> This is free and unencumbered software released into the public domain.
>
> For more information, please refer to <http://unlicense.org>
