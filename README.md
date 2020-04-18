# Relax

Opens a relax notification in Safari every half hour during working hours, only when Do Not Disturb is not active.


## Installation

```shell
export EDITOR=nano
crontab -e
```

```
0,30 9-17 * * 1-5 [[ $(defaults -currentHost read ~/Library/Preferences/ByHost/com.apple.notificationcenterui doNotDisturb) -eq 1 ]] || open -a Safari ~/path/to/relax/index.html
```
