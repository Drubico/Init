## Bluetooth Debian/Deepin?

[Configurar Bluetooth Debian](https://linuxhint.com/configure-bluetooth-debian/)


```
sudo apt-add-repository non-free
sudo apt update
```

## Wifi

```
sudo apt install firmware-iwlwifi -y
```

## Bluetooth

```
sudo apt install rfkill -y
sudo rfkill
sudo rfkill unblock 0
```

## Using GNOME Bluetooth to Connect to Bluetooth Devices 
```
sudo apt install Bluetooth gnome-Bluetooth bluez bluez-tools pulseaudio-module-Bluetooth
sudo systemctl status Bluetooth
sudo systemctl start Bluetooth
sudo systemctl enable Bluetooth
```
## Using Bluedevil to Connect to Bluetooth Devices
```
sudo apt install Bluetooth bluedevil bluez bluez-tools pulseaudio-module-Bluetooth
sudo systemctl status Bluetooth
sudo systemctl start Bluetooth
sudo systemctl enable Bluetooth
```
## Using Blueman to Connect to Bluetooth Devices
```
sudo apt install Blueman

```
