# How to connect to your desired VPN server (AmneziaVPN Client)

This guide explains how you can properly connect to RedHatVPN servers using the AmneziaVPN client

---

## Windows

- Click on the "AmneziaVPN - Windows Client"
- Browser will ask you to save the .exe file - please save it wherever suitable.
- Click on Next up until "Install"
- Once installation completes, the app will launch on it's own - else you can go over to the start menu and launch it.
- Click on "Let's Get Started".
- Download the file shared to you by the RedHatVPN admin/manager. Keep this someonewhere safe and DO NOT SHARE with anyone else.
- Scroll down to find the option - "File with connection settings"
- Find and select the config file you had downloaded earlier.
- The connection will be imported automatically, simply click on "Connect"

---

## Android

- Donwload the "AmneziaVPN" app from Google PlayStore or the RedHatVPN website.
- Open the app
- Click on "Let's Get Started".
- Download the file shared to you by the RedHatVPN admin/manager. Keep this someonewhere safe and DO NOT SHARE with anyone else.
- FOR USERS WHO DOWNLOADED THE CONFIG FROM WHATSAPP : You can find the configuration file from this path
  Internal Storage -> Android > media > com.whatsapp > Whatsapp > Media > WhatsApp Documents > (Upper right corner options AKA Kebab Menu) Sort by > Date (latest/newest - oldest)
  
- Scroll down to find the option - "File with connection settings"
- Find and select the config file you had downloaded earlier.
- The connection will be imported automatically, simply click on "Connect"
- The app may ask for permissions, simply accept all.

---

## iOS

- Donwload the "AmneziaVPN" app from AppStore or the RedHatVPN website.
- Open the app
- Click on "Let's Get Started".
- Download the file shared to you by the RedHatVPN admin/manager. Keep this someonewhere safe and DO NOT SHARE with anyone else.
- Scroll down to find the option - "File with connection settings"
- Find and select the config file you had downloaded earlier.
- The connection will be imported automatically, simply click on "Connect"
- The app may ask for permissions, simply accept all.
  
---

## MacOS

- Testing due
  
---

## Linux

- Testing due, may only work for GUI based Linux distros

---

## 📣 Need Help?

Feel free to open an Issue on https://github.com/RoobusBoi/redhatvpnservices/issues if you encounter any problems!

---
---

# How to connect to your desired VPN server (StrongSwanVPN Client)

This guide explains how you can properly connect to RedHatVPN servers using the AmneziaVPN client

---

## Windows

- Simply run the provided .bat file by the RedHatVPN admin/manager.
- ⊞ (Start Menu) > VPN Settings > Find your RedHatVPN server and click "Connect" - Enter your credentials

---

## Android

- Donwload the "AmneziaVPN" app from Google PlayStore or the RedHatVPN website.
- Open the app
- Click on "Let's Get Started".
- Download the file shared to you by the RedHatVPN admin/manager. Keep this someonewhere safe and DO NOT SHARE with anyone else.
- FOR USERS WHO DOWNLOADED THE CONFIG FROM WHATSAPP : You can find the configuration file from this path
  Internal Storage -> Android > media > com.whatsapp > Whatsapp > Media > WhatsApp Documents > (Upper right corner options AKA Kebab Menu) Sort by > Date (latest/newest - oldest)
  
- Scroll down to find the option - "File with connection settings"
- Find and select the config file you had downloaded earlier.
- The connection will be imported automatically, simply click on "Connect"
- The app may ask for permissions, simply accept all.

---

## iOS

- Due to highly restrictive and secure environment, will require user to join call with a RedHatVPN admin/manager. Has only been tested on a handful of iOS versions.
---

## MacOS

- Due to highly restrictive and secure environment, will require user to join call with a RedHatVPN admin/manager. Has only been tested on a handful of MacOS versions.
  
---

## Linux

- We will install StrongSwan as a Service
- sudo apt update
- sudo apt install strongswan libcharon-extra-plugins
- sudo cp <Location where you stroed the CA certificate provided by the RedHatVPN admin/manager> /etc/ipsec.d/cacerts
- sudo systemctl disable --now strongswan-starter
- sudo nano /etc/ipsec.secrets > add this line
       your_username : EAP "your_password"

- Edit the /etc/ipsec.conf file to configure your client to match the server’s configuration
- config setup

conn RedHatVPN
    right=server_domain_or_IP
    # This should match the `leftid` value on your server's configuration
    rightid=server_domain_or_IP
    rightsubnet=0.0.0.0/0
    rightauth=pubkey
    leftsourceip=%config
    leftid=username
    leftauth=eap-mschapv2
    eap_identity=%identity
    auto=start

- To connect type "sudo systemctl start strongswan-starter"
- To disconnect type "sudo systemctl stop strongswan-starter"

---

## 📣 Need Help?

Feel free to open an Issue on https://github.com/RoobusBoi/redhatvpnservices/issues if you encounter any problems!

---
