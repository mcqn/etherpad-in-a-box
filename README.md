# etherpad-in-a-box
Trivial install of Etherpad onto a Raspberry Pi to aid localised documentation

## Installation

### Pi

1. Install [Ansible](https://www.ansible.com/get-started) on your computer
1. Install the latest [Raspbian lite image](https://www.raspberrypi.org/downloads/raspbian/) onto a micro-SD card
1. Boot the Raspberry Pi with the micro-SD card, while plugged into a network via Ethernet
1. Find out the IP address of the Raspberry Pi
1. Copy your SSH credentials onto the Pi
  ```ssh-copy-id pi@<ip-address-of-the-pi>```
1. Edit the ```hosts``` file so ansible knows which computer to configure.  Change the IP address in it to match the one you just found out.
1. Check you can run commands on the Pi using Ansible
   ```ansible eiab -i hosts -a "hostname" -u pi```
1. Update the Pi
   ```ansible-playbook eiab.yml -i hosts```

## Usage

Once the install is complete, you'll have a local Etherpad server available at [http://etherpad.local:9001](http://etherpad.local:9001)
