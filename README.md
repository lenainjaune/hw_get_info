# hw_get_info
List all hardware infos we can get 

# Linux
## Monitors
Pour obtenir les infos des moniteurs branchés sur un PC il faut utiliser l'[EDID](https://en.wikipedia.org/wiki/Extended_Display_Identification_Data).
Installation sous Debian Buster ```apt install edid-decode read-edid```.
```sh
user@lnj-dell:~# for e in $( ls -1 /sys/class/drm/*/edid ) ; do parse-edid < $e ; done
```
Basé sur [ceci](https://unix.stackexchange.com/questions/114359/how-to-get-edid-for-a-single-monitor/523736#523736)
