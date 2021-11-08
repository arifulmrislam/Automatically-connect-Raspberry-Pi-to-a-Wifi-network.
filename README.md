# Automatically-connect-Raspberry-Pi-to-a-Wifi-network.

Configuring the Wifi network,

When we move our raspberry pi from one place to another place, we lose our Wif connection. At that time, we need a monitor to change the configuration to connect to Wifi. 
So, how can we solve this type of problem?
For this type of problem, we can tell the Raspberry Pi to connect automatically with the Wifi network. We need to edit a file called,

    $ wpa_supplicant.conf
    
At first, connect Raspberry Pi with the laptop by Putty.
To open the configuration file with the following command,

    $ sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
    
Scroll down and finally add these following commands to configure our network,

    network={
       ssid="Test Wifi Network" 
       psk="SecretPassWord"
    }
    
Remember that to replace SSID and PSK with existing network names and passwords. After setting everything,  save and close the file by pressing Ctrl+X followed by Y. At this point the Raspberry Pi should automatically connect to the network.
To check the network connection by running the following command:

    $ ifconfig wlan0
