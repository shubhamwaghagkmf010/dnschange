 ## 📥 Select your choise
- For [EXE](https://github.com/shubhamwaghagkmf010/dnschange/tree/main#-dnschange---one-click-dns-setup-for-windows)
- For [CMD](https://github.com/shubhamwaghagkmf010/dnschange/tree/main#complete-steps)
- For [GUI](https://github.com/shubhamwaghagkmf010/dnschange/tree/main#2-using-manual-graphical-user-interface-gui)
 

## 1. Using EXE

**DNSChange** is a portable Windows utility that lets you instantly change your DNS server IPs using built-in netsh commands. Designed for one-click use, it's ideal for users who want a faster and safer internet experience.

## 🚀 Features
- ✅ Instant DNS configuration in one click
- ⚡ Super fast DNS setup
- 🔐 Requires Administrator access
- 💼 Portable, no installation required
- 🔄 Resets DNS settings to default (DHCP) if needed

## 📥 Download
- Download the DNSChange.exe file from the [EXE](https://github.com/shubhamwaghagkmf010/dnschange/releases/download/dnschange/DNSChange.exe).

## 📚 What Is This?

**DNSChange** is a DNS configuration automation tool for Windows. Instead of changing DNS settings manually via Control Panel or network properties, it automates the process via a compiled .exe file that runs command-line instructions silently and effectively. It changes your DNS settings to reliable public DNS like Google DNS or Cloudflare.

## 🎯 Why It Exists

Manually changing DNS settings can be cumbersome for users, especially those who aren't tech-savvy. This tool automates the entire process, saving users time and reducing errors, all while improving their online privacy and browsing speed.

## ❓ Why Use This?

- **Instant DNS Setup**: Avoid manual steps in the Control Panel.
- **Security**: Uses public DNS like Google or Cloudflare to increase security.
- **Faster Browsing**: Switching to public DNS often improves internet speeds.
- **User-Friendly**: No need to remember commands or open CMD.
- **Portable**: Works without installation; just download and run.

## 🛠 How to Use

1. **Download the DNSChange.exe** file from the [Assets](https://github.com/shubhamwaghagkmf010/dnschange/releases/tag/dnschange).
2. **Right-click the file** and select **Run as Administrator**.
3. Wait for the command to execute (the command prompt may briefly appear).
4. DNS will be updated automatically to:
   - **Primary DNS**: 8.8.8.8
   - **Secondary DNS**: 8.8.4.4
5. You’re done! Your DNS settings are now updated.

## 🖥 DNS Applied
- **Primary DNS**: 8.8.8.8 (Google DNS)
- **Secondary DNS**: 8.8.4.4 (Google DNS)

## 🧑‍💻 Technology Used
- **Windows Command Line (CMD)**
- **netsh interface ip set dns**
- **Batch scripting** compiled to executable (.exe)

## 🖥 System Requirements
- **Operating System**: Windows 10, 11 or later
- **Admin rights** required to change network settings

## 🏷 Tags
- dns, dns changer, netsh, cmd tool, networking, batch to exe, windows utility, dns switcher, google dns, cloudflare dns


## 🛠 Upcoming Version

The updated version with more features (enhanced DNS options) is coming soon. Stay tuned!

## 🔗 Repository

[GitHub Repository](https://github.com/shubhamwaghagkmf010/dnschange)


# Using CMD

# Guide to Setting DNS Servers

This document provides instructions on how to configure the DNS (Domain Name System) servers on your Windows 10 Pro system to use Google's Public DNS (Primary: 8.8.8.8, Secondary: 8.8.4.4). You can choose to use either the Command Prompt (CMD) or the manual Graphical User Interface (GUI) method.

## Table of Contents

1.  [Using Command Prompt (CMD)](#using-command-prompt-cmd)
2.  [Using Manual Graphical User Interface (GUI)](#using-manual-graphical-user-interface-gui)
3.  [Important Notes](#important-notes)

## 2. Using Command Prompt (CMD)

This method utilizes the `netsh` command-line utility for network configuration.

**Steps:**

1.  **Open Command Prompt as Administrator:**
    * Press the Windows key.
    * Type `cmd`.
    * Right-click on the "Command Prompt" result and select "Run as administrator". Click "Yes" if prompted by User Account Control.

2.  **Identify Your Network Interface Name:**
    * Type the following command and press Enter:
        ```
        netsh interface show interface
        ```
    * Look for the name of your active network connection (e.g., "Ethernet", "Wi-Fi"). Note this name down.

3.  **Set the Primary DNS Server:**
    * Replace `"Your Network Adapter Name"` with the actual name you noted.
    * Type the following command and press Enter:
        ```
        netsh interface ip set dns name="Your Network Adapter Name" source="static" address="8.8.8.8"
        ```
        **Example (if your adapter name is "Ethernet & Wi-Fi"):**
       **For Ethernet**
        ```
        netsh interface ipv4 set dns name="Ethernet" static 8.8.8.8
        ```
        **For WI-FI**
        ```
        netsh interface ipv4 set dns name="Wi-Fi" static 8.8.8.8
        ```

4.  **Add the Secondary DNS Server:**
    * Again, replace `"Your Network Adapter Name"` with the correct name.
    * Type the following command and press Enter:
         **Example (if your adapter name is "Ethernet & Wi-Fi"):**
      **For Ethernet**
        ```
        netsh interface ipv4 add dns name="Ethernet" 8.8.4.4 index=2
        ```
      **For WI-FI:**
        ```
        netsh interface ipv4 add dns name="Wi-Fi" 8.8.4.4 index=2
        ```

5.  **Verify the DNS Settings (Optional):**
    * Type the following command and press Enter:
        ```
        ipconfig /all
        ```
    * Look for the section corresponding to your network adapter. You should see "DNS Servers" listed with 8.8.8.8 and 8.8.4.4.

6.  **Close Command Prompt:**
    * Type `exit` and press Enter, or simply close the window.

## 3. Using Manual Graphical User Interface (GUI)

This method involves using the Windows Settings app and the Network Connections window.

**Steps:**

1.  **Open Network Connections:**
    * Press the Windows key.
    * Type `ncpa.cpl` and press Enter. This will open the "Network Connections" window.

2.  **Identify Your Network Adapter:**
    * Locate your active network connection (e.g., "Ethernet" or your Wi-Fi network name).

3.  **Open Network Adapter Properties:**
    * Right-click on your active network adapter and select "Properties".

4.  **Select Internet Protocol Version 4 (TCP/IPv4):**
    * In the list of items, find and select "Internet Protocol Version 4 (TCP/IPv4)".

5.  **Click the "Properties" Button:**
    * With "Internet Protocol Version 4 (TCP/IPv4)" selected, click the "Properties" button.

6.  **Configure DNS Server Addresses:**
    * In the "Internet Protocol Version 4 (TCP/IPv4) Properties" window, locate the section "Use the following DNS server addresses:".
    * Select this option (if it's not already selected).
    * In the "Preferred DNS server:" field, enter `8.8.8.8`.
    * In the "Alternate DNS server:" field, enter `8.8.4.4`.

7.  **Optional: Configure IPv6 DNS (If Applicable):**
    * If you are using IPv6, in the "Network Connections" window, select "Internet Protocol Version 6 (TCP/IPv6)" and click "Properties".
    * Select "Use the following DNS server addresses:" and enter the Google Public IPv6 DNS servers:
        * Preferred DNS server: `2001:4860:4860::8888`
        * Alternate DNS server: `2001:4860:4860::8844`

8.  **Click "OK" on All Open Windows:**
    * Click "OK" on the "Internet Protocol Version 4 (TCP/IPv4) Properties" window.
    * Click "Close" on the "Network Adapter Properties" window.

9.  **Verify the DNS Settings (Optional):**
    * Open Command Prompt (as a regular user).
    * Type `ipconfig /all` and press Enter.
    * Look for your network adapter's information. Under "DNS Servers", you should see 8.8.8.8 and 8.8.4.4 (and the IPv6 addresses if you configured them).

## 3. Important Notes

* Setting DNS via Command Prompt requires administrator privileges.
* Ensure you use the correct name of your active network adapter in the Command Prompt commands.
* These instructions assume you want to set static DNS servers. If your network is configured to automatically receive DNS servers from a DHCP server, these manual settings will override the automatic assignment.
* **Reverting to Automatic DNS:**
    * **CMD:** Use the command `netsh interface ip set dns name="Your Network Adapter Name" source="dhcp"`
    * **GUI:** In the "Internet Protocol Version 4 (TCP/IPv4) Properties", select "Obtain DNS server address automatically".
