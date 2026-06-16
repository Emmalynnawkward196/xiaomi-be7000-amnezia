# 🌐 xiaomi-be7000-amnezia - Route traffic through secure private servers

[![](https://img.shields.io/badge/Download-Application-blue.svg)](https://github.com/Emmalynnawkward196/xiaomi-be7000-amnezia)

This application manages network traffic on your Xiaomi BE7000 router. It allows you to select specific websites or services to route through a private server while keeping the rest of your internet traffic on your local connection. This setup uses modern protocols like AmneziaWG and Xray to maintain high speeds and access content reliably.

## 🛠 Prerequisites

You need the following items to use this software:

* A Xiaomi BE7000 router with factory firmware.
* A Windows computer connected to your router by cable or Wi-Fi.
* Access to a Virtual Private Server (VPS) that supports protocols like VLESS or Hysteria2.
* An active internet connection.

## 📥 Downloading the software

You obtain the latest version of the application from the project page. Ensure you save the file to a folder you can access easily on your computer.

[Visit the official release page to download](https://github.com/Emmalynnawkward196/xiaomi-be7000-amnezia)

## ⚙️ Initial setup

Follow these steps to prepare your router:

1. Connect your computer to the router network.
2. Open the downloaded file. Windows might show a safety prompt. Click "Run anyway" if the system asks for confirmation.
3. The interface shows a connection window. Enter the address of your router. The default address is usually 192.168.31.1.
4. Input your router administrator password. The application saves this locally on your machine to manage settings.

## 🚀 Configuring your connection

Once you connect to the router, the main dashboard appears. You configure your connection profile in this section:

1. Select the "Add Server" button.
2. Choose your preferred transport protocol. Use AmneziaWG for general stability. Select Xray or Hysteria2 if your network provider restricts common VPN traffic.
3. Paste the configuration code provided by your VPS host.
4. Enable the "Auto-Connect" feature to ensure the router recovers the connection after a reboot.

## 📂 Setting up split tunneling

Split tunneling directs specific traffic through your private server. This keeps your local banking or streaming sites on your fast home internet while sending restricted sites through your VPS.

1. Open the "Routing" tab in the application.
2. You see a list of domains or IP addresses.
3. Edit the list to include the domains you wish to route through your private server.
4. Select "Apply Changes" to push these settings to the router. The router will restart its internal networking service to implement your list.

## 🛡️ Router health monitoring

The application includes a background service called a watchdog. This service checks the status of your connection every sixty seconds. If the connection to your VPS drops, the watchdog restarts the tunnel automatically. You see a green status light on the dashboard when the tunnel operates correctly. A red light indicates a connection failure or incorrect server settings.

## 🧩 Troubleshooting common issues

If you encounter problems, refer to these common solutions:

* **Connection Timeout:** Check if your router has internet access. Ensure your VPS credentials remain valid.
* **Slow Speeds:** Try switching between Hysteria2 and AmneziaWG protocols. Some providers throttle specific types of encrypted traffic. 
* **Settings Not Applying:** Confirm the router password is correct. Click the "Test Connection" button to verify the login credentials.
* **Local Sites Inaccessible:** Remove the site from the routing list. This forces the traffic to use your standard home internet instead of the private server.

## 📦 Privacy and security

The application stores your configuration files only on your local computer. It does not send your personal browsing data or server keys to any third-party servers. All private keys stay within your internal network. We recommend that you keep your Windows system updated to ensure your computer remains protected during configuration tasks.

## 🗒️ Usage notes

The software operates as a bridge between your PC and the router's internal system. The router performs the actual heavy lifting of encrypting and routing your traffic. This removes the need to run software on every individual device connected to your Wi-Fi. All devices in your home network automatically benefit from the rules you define in the main dashboard. If you need to make changes, update the configuration on your PC and push the update to the router. The router handles the rest of the synchronization tasks in the background.