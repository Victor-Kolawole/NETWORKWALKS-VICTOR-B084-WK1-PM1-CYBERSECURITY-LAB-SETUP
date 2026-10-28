# NETWORKWALKS-VICTOR-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux. The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

🎯 Objectives

The main objectives of this project are to:

Install and configure VirtualBox.

Install/import Kali Linux as a virtual machine.

Create a private NAT Network for the cybersecurity lab.

Configure network connectivity for Kali Linux.

Assign a consistent IP address to the Kali VM.

Verify network connectivity and DNS resolution.

Take a clean VM snapshot for recovery.

Document the complete setup process.

Prepare the environment for future cybersecurity projects.

🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

Network reconnaissance

Port scanning

Vulnerability assessment

Packet analysis

Web security testing

Exploitation practice

Security-tool experimentation

⚠️ Important: 

This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.



# ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 💻 Host OS | Windows 11 |
| 🧠 Host RAM | 16 GB |
| ⚡ Processor | Intel Core i7  |
| 🧰 Hypervisor | VirtualBox |
| 🐉 Security OS | Kali Linux |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24  |
| 🚪 Default Gateway | 10.0.0.1  |
| 🚪 DNS Server | 8.8.8.8  |

# 🛡️ Lab Setup Procedure
## Step 1: Install VirtualBox

Oracle VirtualBox was installed to run Kali Linux in a virtual machine without replacing the Windows host operating system.

*Tool:* Oracle VirtualBox was installed as the hypervisor.

## Step 2: Create the NAT Network

A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled
<img width="1895" height="973" alt="Screenshot Network settings" src="https://github.com/user-attachments/assets/5d4e7a76-5594-45a1-bad5-b815cd9adc6a" />
A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.
## Step 3: Import Kali Linux
The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

*Configuration:*
- Operating System: Kali Linux
- RAM: 2048 MB
- Network Adapter: NAT Network
- Adapter Type: Intel PRO/1000 MT Desktop
 <img width="1919" height="939" alt="Screenshot Kali-linux" src="https://github.com/user-attachments/assets/4e38e2fa-902c-40bf-ae3a-5ff55759b032" />
A shared folder was also configured for transferring required files between the host operating system and the Kali VM.

## Step 4: Configure the Kali Linux Network

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

- IP Address: 10.0.0.2
- Subnet Mask: 255.255.255.0
- Gateway: 10.0.0.1
- DNS: 8.8.8.8

A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.
<img width="1919" height="1027" alt="Screenshot Kali linuz network settings" src="https://github.com/user-attachments/assets/7f666dc4-b9a0-4bc6-a112-48ab282bed2e" />

## Step 5: Verify Network Connectivity
After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:

- Clean Kali - Network Setup

  The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.

