## Termux Disable Procces 9 Kill (No ROOT | NO COMPUTER)
> **a help for those who don't have root or computer to disable the termux error processes**

## Tutorial (Video):

<video autoplay loop style="width:100%; heigth: auto; position:absolute; z-index; -1;">
   <source src="TermuxSignalErrorResolved.mp4" type="video/mp4" />

</br>

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
