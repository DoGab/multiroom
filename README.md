# Multiroom
Control your Samsung Multiroom Speakers with a simple to use bash script. 
It is based on the git project `https://github.com/bacl/WAM_API_DOC`.

## Preparation
The script only required `curl`. You may want to adjust your `PATH` or/and `CURL` variables in the scripts header to match your customization.
```
PATH=/sbin:/usr/sbin:/bin:/usr/bin

CURL="/usr/bin/curl"
PORT="55001"
```

## Usage
The following options can be used to control the speakers. If you have assigend static ip-adresses to your speaker you don't need the `search` parameter.
All of the functions without the `UUID` one are tested and should be working.
```
~/github/multiroom$ bash multiroom.sh --help
Usage:
    multiroom.sh help (print the scripts usage)
    multiroom.sh search (search for speakers)
    multiroom.sh <Speaker-IP> UUID OBJECTID [OBJECTID OBJECTID ...] [volume]
    multiroom.sh <Speaker-IP> fav1/fav2/fav3/radio1/radio2/radio3/radio4/radio5/radio6/radio7 [volume]
    multiroom.sh <Speaker-IP> play/pause/stop  (song: play/pause  radio: stop)
    multiroom.sh <Speaker-IP> next/previous
    multiroom.sh <Speaker-IP> getmute
    multiroom.sh <Speaker-IP> mute on/off
    multiroom.sh <Speaker-IP> volume (Set volume to value from 0 to 30)
    multiroom.sh <Speaker-IP> getvolume
    multiroom.sh <Speaker-IP> volumeup (volume + 1)
    multiroom.sh <Speaker-IP> volumedown (volume - 1)
    multiroom.sh <Speaker-IP> show title/id (show information of played song)
    multiroom.sh <Speaker-IP> list (show uuid and objectid's of actual playlist)
    multiroom.sh <Speaker-IP> presets all/fav1/fav2/fav3/radio1/radio2/radio3
    multiroom.sh <Speaker-IP> name (speaker name)
    multiroom.sh <Speaker-IP> soundshare (set input to soundshare = TV-connect)
    multiroom.sh <Speaker-IP> aux (set input to aux)
    multiroom.sh <Speaker-IP> bluetooth (set input to bluetooth)
```
