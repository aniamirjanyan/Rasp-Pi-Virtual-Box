### Install on Raspberry Pi

1. Installing Mycodo 
```
$ curl -L https://kizniche.github.io/Mycodo/install | bash
```

Go to `https://127.0.0.1` to check if the installation was successful. It will ask you to insert login credentials (make sure the password is at least 8 characters).


2. Clone MaxPonics Repository 

Open a terminal and run this command
```
sudo git clone https://github.com/MaxPonics/HydroController.git
```

3. Change the folders

Navigate to `/home/pi/HydroController/MaxPonics/mycodo/mycodo_flask/`

Copy the folder `templates`

Navigate to `/home/pi/Mycodo/mycodo/mycodo_flask/`

Delete the present folder `templates` and paste the new one. 

4. Restarting mycodo

Run the following commands

```
sudo service mycodoflask restart
sudo service nginx restart
```

Go to `https://127.0.0.1` to check the changes. 
