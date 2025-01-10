<p align="center">
<img src="https://i.imgur.com/r8S0B8F.png" alt="vpn diagram"/>
</p>

# Azure Virtual Machine and VPN Lab

This tutorial walks you through setting up a virtual machine in Microsoft Azure, testing VPN connections, and observing the changes in IP addresses.

---

## Part 1: Create a Virtual Machine in Azure

1. **Access Your Public IP Address**
   - On your own machine, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of your public IP address and save it in a text file for reference.

2. **Create a Resource Group**
   - Log into your Azure Portal: [Azure Portal](https://portal.azure.com/).
   - Navigate to **Resource Groups** and click **Create**.
   - Provide the following:
     - **Resource Group Name**: `MyAzureVPNLab`
     - **Region**: Select a region near you.
   - Click **Review + Create**, then **Create**.

3. **Create a Virtual Machine**
   - Navigate to **Virtual Machines** in the Azure Portal and click **Create**.
   - Select **Azure Virtual Machine**.
   - Fill out the following:
     - **Name**: `MyWindowsVM`
     - **Region**: Choose a region close to your geographic location or country from your current location.
     - **Image**: Windows 10 22H2.
     - **Size**: Select a size that has at least 2vcpus, and 8GiB memory.
     - **Administrator Username and Password**: Set your credentials.
   - Acknowledge licensing agreement & ensure **Inbound Port Rules** to allow RDP (Remote Desktop Protocol).
   - Click **Review + Create**, then **Create**.

<p>
   
![VPN SS 1](https://github.com/user-attachments/assets/623313db-c13a-4362-bedf-4175c9677194)

</p>

4. **Log into the Virtual Machine**
   - After the VM is created, navigate to it in the Azure Portal.
   - Copy the **Public IP Address** of your VM.
   - Use Remote Desktop to connect to the VM:
     - **Remote Desktop Address**: Enter the Public IP Address of the VM.
     - **Username and Password**: Use the credentials you created earlier.
   - Once connected, open a web browser on the VM.

<p>
   
![vpn ss 2](https://github.com/user-attachments/assets/e92d2eff-5a0f-4fb1-9d8a-daa5338c1f87)

</p>

5. **Check the VM's Public IP Address**
   - In the VM, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of the VM's public IP address and save it in a text file.

---

## Part 2: Sign Up for ProtonVPN and Test the VPN Connection

1. **Sign Up for ProtonVPN**
   - On your actual computer, go to [ProtonVPN Sign-Up](https://account.protonvpn.com/signup?plan=free&language=en).
   - Create a free account.

2. **Download ProtonVPN Client**
   - In your VM, go to [ProtonVPN Download](https://protonvpn.com/download/).
   - Download and install the ProtonVPN client.

3. **Log Into ProtonVPN**
   - Open the ProtonVPN client in the VM.
   - Log in using your ProtonVPN account credentials: [ProtonVPN Login](https://account.protonvpn.com/login).

4. **Connect to a VPN Server**
   - In the ProtonVPN client, choose a VPN server in a area different from your actual computer's location (Proton VPN requires payment to change countries).
   - Connect to the VPN server.

<p>
   
![VPN SS 3](https://github.com/user-attachments/assets/522d4570-2aa5-4246-8512-09c237c4f46d)

</p>

5. **Check the VPN's Public IP Address**
   - In the VM, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of the new IP address and save it in a text file.

---

## Notes and Observations

- Save all IP addresses and observations in a text file for documentation purposes.
- Compare the behavior of websites and the changes in IP addresses to understand the effects of geographic location and VPN usage.
- From this lab, here are my documented IP addresses & their changes:

<p>
   
![VPN SS 4](https://github.com/user-attachments/assets/fd70a33c-a6ce-41cd-ad57-fd6fde57716c)

</p>

<p>
   
![VPN SS 5](https://github.com/user-attachments/assets/8872a1a6-53c0-495f-8248-36f39d455f22)

</p>

---
