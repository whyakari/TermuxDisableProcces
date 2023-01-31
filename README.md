## Termux Disable Proccess Error 9 Kill (No ROOT | NO COMPUTER)
> **a help for those who don't have root or computer to disable the termux error processes**

## Tutorial (Video):
[![Video Uploaded On Youtube](https://i3.ytimg.com/vi/IhK55QfWdYc/hqdefault.jpg)](https://youtu.be/IhK55QfWdYc)

### Requirements:
 - Android 12+
 - Connection Wi-fi 

#### Deactivation Instructions (ADB):
> *On an ADB console, paste the following commands on the following order:*

```
 adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
```

```
 adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
```

```
 adb shell settings put global settings_enable_monitor_phantom_procs false
```

### if your cell phone is Samsung brand, you may have to do this first (Termux/terminal):
```
 export ADB_SERVER_SOCKET=localfilesystem:$(pwd)/adb_socket
 adb start-server
 adb devices
```

#### Download of Termux *(with Monet-You)*:
[<img src="https://raw.githubusercontent.com/HardcodedCat/termux-monet/master/art/ic_monet.svg" width="190">](https://github.com/HardcodedCat/termux-monet/releases)    
> download termux with the latest version. it's important to keep up to date!
