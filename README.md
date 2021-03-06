# Rasp-Pi-Virtual-Box

Install Virtualbox from [here](https://www.virtualbox.org/wiki/Downloads).

Download the Debian Buster with Raspberry Pi Desktop ISO from [here](https://www.raspberrypi.org/software/raspberry-pi-desktop/).

### Creating the Raspberry Pi VirtualBox 

- Start VirtualBox and click New.
- Enter a name, change the Type to Linux, and version to Debian (64-bit).
- Select at least 1024 MB RAM. 
- Select Create a virtual hard disk now.
- Select VDI (VirtualBox Disk Image).
- Select Dynamically allocated.
- Allocate at least 12 GB on the next screen.
- Click Settings.
- Click Storage on the left menu.
- Under Controller: IDE, select Empty, then under Attributes on the right, click the disc icon next to Optical Drive, then select Choose Virtual Optical Disk File and select the Raspbian ISO that was downloaded.
- Click OK.
- Start the virtual machine by clicking Start.
- --------------------------------------------
- Select install.
- Select your language.
- On the Partition discs screen, select Guided - use entire disk.
- On the next screen, select the only disk that's presented.
- On the next screen, select All files in one partition (recommended for new users).
- On the next screen, select Finish partitioning and write changes to disk.
- On the next screen, select <Yes> to the Write the changes to disks? 
- On the Install the GRUB boot loader on a hard disk screen, select <Yes> to the Install the GRUB boot loader to the master boot record?
- On the next screen, select /dev/sda, then press Enter.
- Select 'Continue'.
- --------------------------------------------
Recommended to do:
```
$ sudo apt update && sudo apt upgrade 
```

### Installing InfluxDB 
```
$ sudo apt-get update
$ sudo apt-get install influxdb
$ sudo systemctl enable influxdb 
$ sudo systemctl restart influxdb 
$ sudo systemctl status influxdb 
```

### Installing Mycodo 
```
$ curl -L https://kizniche.github.io/Mycodo/install | bash
```

Go to `https://127.0.0.1` to check if the installation was successful. 

It will ask you to insert login credentials (make sure the password is at least 8 characters).

If the Daemon Status is 'Not Running' try this command 
$ sudo ~/Mycodo/env/bin/python ~/Mycodo/mycodo/mycodo_daemon.py
