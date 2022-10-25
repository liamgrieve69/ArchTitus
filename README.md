
## Boot Arch ISO

From initial Prompt type the following commands:

```
pacman -Sy git
git clone https://github.com/ChrisTitusTech/ArchTitus
cd ArchTitus
./archtitus.sh
```

### System Description
This is completely automated arch install. It includes prompts to select your desired desktop environment, window manager, AUR helper, and whether to do a full or minimal install. The KDE desktop environment on arch includes all the packages I use on a daily basis, as well as some customizations.

### No Wifi

You can check if the WiFi is blocked by running `rfkill list`.
If it says **Soft blocked: yes**, then run `rfkill unblock wifi`

After unblocking the WiFi, you can connect to it. Go through these 5 steps:

#1: Run `iwctl`

#2: Run `device list`, and find your device name.

#3: Run `station [device name] scan`

#4: Run `station [device name] get-networks`

#5: Find your network, and run `station [device name] connect [network name]`, enter your password and run `exit`. You can test if you have internet connection by running `ping google.com`, and then Press Ctrl and C to stop the ping test.

An issue is easier to resolve if it contains a few important pieces of information.
1. Chosen configuration from /configs/setup.conf (DONT INCLUDE PASSWORDS)
1. Errors seen in .log files
1. What commit/branch you used
1. Where you were installing (VMWare, Virtualbox, Virt-Manager, Baremetal, etc)
    1. If a VM, what was the configuration used.
