## Termux Disable Proccess Error 9 Kill (No ROOT | NO COMPUTER)

> **A guide for those who don't have root or a computer to disable the termux error processes**

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

#### If ur device's brand is Samsung, you may have to do this first (Termux/terminal):
> ```sh
> export ADB_SERVER_SOCKET=localfilesystem:$(pwd)/adb_socket
> adb start-server
> adb devices
> ```

---

Check this out if you would like to re-enable Phantom processes
https://www.reddit.com/r/termux/comments/11tkms8/comment/jcjuldr


> **Make sure to download the latest termux version. It's important to keep up to date!**
