`pacman -Ss repo` to search for repo
`sudo pacman -S repo` to install repo 
`sudo nano /etc/pacman.conf` to change `color` and allow parallel downloads + `ILoveCandy` to change dL bar into pacman 
```
sudo systemctl enable bluetooth && sudo systemctl start bluetooth
sudo modprobe btus
sudo pacman -S bluez blueman bluez-utils
```
install bluetooth at boot and start service

```
sudo pacman -S p7zip unrar tar rsync git neofetch htop exfat-utils fuse-exfat ntfs-3g flac jasper aria2
```
various utils needed for general purposes

```
sudo pacman -S jdk-openjdk
```
java install

```
sudo pacman -S amd-ucode
```
update amd cpu 

While using Pacman in Arch Linux, you may find that there are limitations on which GUI applications you can install. For example, popular programs like Google Chrome, VSCode, and Timeshift cannot be installed through Pacman. Instead, you will need to rely on the Arch User Repository (AUR) or Flatpak to install additional software.

Yay is a popular aur helper, which simplifies the process of installing and managing packages from AUR.

```
sudo pacman -S --needed base-devel git
```
```
cd yay
```
``pacman -S --needed git base-devel
`git clone https://aur.archlinux.org/yay.git
`cd yay
`makepkg -si````
```
makepkg -si
```
```
sudo pacman -S flatpak
```
install yay to install stuff from the AUR and install flatpak

```
sudo pacman -S firefox libreoffice-fresh vlc gimp thunderbird 
```
Common software 

In Arch Linux, it’s a good idea to have multiple kernels installed as a safety precaution. If one kernel fails to boot, you can use another one to start the operating system. For instance, I suggest installing the LTS kernel by running a command, as it’s generally considered to be more stable than the latest kernels. Additionally, you can explore other kernels like Zen and Hardened.

```
yay -Sy timeshift
```
similar to windows system restore in case of need of a backup

An uncomplicated Firewall (UFW) is a security tool that can help protect your computer from network traffic and block malicious software from accessing your network via the internet. To set up a firewall:
```
sudo pacman -S ufw```
sudo systemctl enable ufw```
sudo systemctl start ufw
```
UFW allows you to have full control over enabling and disabling ports. For example, if you’re running an SSH server on port 22, you can disable this port to prevent connections from remote computers.

```
sudo ufw deny 22/tcp
```
Preload is a daemon service that runs in the background. It Analyzes the user behavior and tracks what applications are frequently running by the user.

Based on these analyses, it predicts what applications the user might run next and fetches those binaries and their dependencies into memory and hence increasing the start-up time of the applications.


You Can install the preload by running the below commands.

```
yay -S preload```
sudo systemctl enable preload && sudo systemctl start preload
`
`
