# homeserver
My homeserver setup


### Install debian 
The Debian GUI installer is pretty good, try to get the non-free image if you foresee that you would need non-free drivers and such.
### Set up ssh server:
Disallow password log in, disallow root log in
## Install zsh & oh-my-zsh  

* `ZSH_THEME="bira"`  
* `COMPLETION_WAITING_DOTS="true"`  
* `export EDITOR='vim'`  
* `export LANG=en_US.UTF-8`  
* `umask 027`  
* `setopt nosharehistory`  
* `w`  

## Router port forward ssh to a non-standard port
## Install HDD monitoring tools:
* Install the smartmontools package that contains smartd.
* Edit `/etc/default/smartmontools`, add these line: `start_smartd=yes` and `smartd_opts="--interval=28800"`
* interval = 8h
* edit `/etc/rsyslog.conf` and add `if ($msg contains "smartd") then /var/log/smartd.log` to log smartd 
* add `cat /proc/mdstat` to `.zshrc`
* add `DEVICESCAN -d removable -n standby -m ankel -M exec /usr/share/smartmontools/smartd-runner` to `/etc/smartd.conf`
## Install services that we need
