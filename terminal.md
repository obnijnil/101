# Shell

##`sudo` without password

You have to edit /etc/sudoers file by running
```shell
sudo visudo
```
in the terminal, then add this line at the bottom
```shell
username ALL=(ALL) NOPASSWD: ALL # Replace username with your name.
```
After this, you can `sudo whatever_you_want` without the password.

## cron

*-nix scheduler.

```shell
crontab -l # List all your cron jobs.
crontab -e # Edit your cron jobs.
```

How to create a cron job?

```
*[minute] *[hour] *[day of month] *[month] *[week day] [shell script goes here]
```

e.g.

```
1 * * * * * osascript -e "display notification \"$(date)\" with title \"Title\" subtitle \"Subtitle\" sound name \"Purr\""
```

# Ruby

## Can't install gems?

> Use RVM (or other managers like chruby, rbenv, etc.) when doing Ruby development.

The mac-come-with Ruby is installed into /usr/bin which is not writable for common users (even sudo) due to Mac OS X SIP (System Integrity Protection), like
```shell
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /usr/bin directory.
```
Those ruby version managers would install ruby into a developer-available location, e.g /usr/local/bin. In this case, gems can be installed without the above error.

Consider keeping using the mac-come-with Ruby, you still can install gems in other developer-available locations, by specifying the location:
```shell
gem install jekyll -n/usr/local/bin
```
And you can even make it the default location when installing gems, by adding below parameters into ~/.gemrc:
```shell
gem: -n/usr/local/bin
```
Then just use:
```shell
gem install jekyll
```
