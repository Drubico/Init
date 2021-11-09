```
nano ~/.bashrc
```
alias refrescar='sudo apt update -y && sudo apt upgrade -y && sudo apt clean && sudo apt autoclean && sudo apt autoremove && sudo apt remove'

alias cleancache='sudo sync; echo 1 > /proc/sys/vm/drop_caches
\sync; echo 2 > /proc/sys/vm/drop_caches
\sync; echo 3 > /proc/sys/vm/drop_caches'

```
source ~/.bashrc
```
