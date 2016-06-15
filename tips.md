# `sudo` without password

You have to edit /etc/sudoers file by running
```shell
sudo visudo
```
in the terminal, then add this line at the bottom
```shell
username ALL=(ALL) NOPASSWD: ALL # Replace username with your name.
```
After this, you can `sudo whatever_you_want`.
