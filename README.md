# freebsd-sshd-disable-password-authentication
freebsd-sshd-disable-password-authentication

Edit the file /etc/ssh/sshd_config

Change these three lines:
```
PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM yes
```
Restart SSH server:
```
# sh /etc/rc.d/sshd restart
Restarting sshd.
```
Becareful, user/password can not work anymore, only certificate authentication can, before do this, make sure create certificate authentication method first.
