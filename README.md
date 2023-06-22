## Termux Disable Proccess Error 9 Kill (No ROOT | NO COMPUTER)

> **a help for those who don't have root or computer to disable the termux error processes**

-----
### Requirements
>  - Android 12+ (tested only AOSP)
>  - Connection with Wi-Fi

---

### Tutorial (Video)
> [![Video Uploaded On Youtube](https://i3.ytimg.com/vi/IhK55QfWdYc/hqdefault.jpg)](https://youtu.be/IhK55QfWdYc) 

### Deactivation Instructions (ADB):
> *On an ADB console, paste the following commands on the following order:*

> ```sh
> adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
> ```

> ```sh
> adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
> ```

> ```sh
> adb shell settings put global settings_enable_monitor_phantom_procs false
> ```

---

#### if ur device is Samsung brand, ur may have to do this first (Termux/terminal):
> ```sh
> export ADB_SERVER_SOCKET=localfilesystem:$(pwd)/adb_socket
> adb start-server
> adb devices
> ```

---

#### Download of Termux *(with Monet-You)*:
[<img src="https://raw.githubusercontent.com/HardcodedCat/termux-monet/master/art/ic_monet_dark.svg" width="120x50">](https://github.com/HardcodedCat/termux-monet/releases)    
> **download termux with the latest version. it's important to keep up to date!**
