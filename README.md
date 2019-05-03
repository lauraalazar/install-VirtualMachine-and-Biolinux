# install-VirtualMachine-and-Biolinux
How to set up a virtual machine in windows that allows linux for sequence analyses

## Download and install VirtualBox
https://www.virtualbox.org/wiki/Downloads
run the VirtualBox-version-Win.exe 

## Download Biolinux
http://environmentalomics.org/bio-linux-installation/
Follow "Running Bio-Linux as a VM with VirtualBox"

## Add GuestAdditions
Adding them from the option Device -> Insert CD Guest Additions... did not work, so it needed to be manually run:
```
sudo mkdir /media/GuestAdditionsISO
sudo mount /paht/to/VBoxGuestAdditions.iso /media/GuestAdditionsISO
cd /media/GuestAdditionsISO
sudo ./VBoxLinuxAdditions.run
```


## Install package manager Conda

Follow instruction from https://genomics.sschmeier.com/ngs-tools/index.html and after installation and environment set up, restart VM to get the rigth PATH.

### To update R from 3.2 to 3.4 with Conda
```
conda create -n myrenv r=3.4.1
source activate myrenv
```
