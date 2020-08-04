# raspberry-pi

### To Flash memmory card

- Download the image from https://www.raspberrypi.org/downloads/raspberry-pi-os/
- Flash the image by using https://www.balena.io/etcher/


### Create first ssh connection
- Once the flashing completed, create a new `ssh` file inside `boot` folder.
```cmd
touch ssh
```
- Add details inside `wpa_supplicant.conf` file(File Location : `/boot/wpa_supplicant.conf`)

```cmd

vi wpa_supplicant.conf

# add the following details
#
# ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
# update_config=1
# country=US
#
# network={
#  ssid="wifi"
#  psk="password"
#  key_mgmt=WPA-PSK	
# }
#
#
```
- Save the file and insert memmory card in ras-pi

### Get device names from a wifi network

```cmd
sudo apt-get install arp-scan

sudo arp-scan 192.168.1.0/24

```
### Connecting to pi

- Create a new ssh coonection to the ras-pi by 

```cmd
ssh pi@192.168.3.11
```
default username: pi
default password: raspberry

