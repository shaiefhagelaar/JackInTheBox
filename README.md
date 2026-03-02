# JackInTheBox Clawbot
AI Bot based on Kali hosted in the cloud.

# Video
https://youtu.be/C5ir_rQ4L4g?si=kqcTDL77hKjZwTE8

# Intro 
The video below shows how to set up a clawbot as a personal AI assistent on a VPS (Virtual Private Server) that you can use with a messaging app like: Whatsapp/Signal/Telegram. It's a basic set up to get a AI Bot running on a server which I'll use to help me out with some cybersecurity stuff. Do note that this is at your own risk, know your ethical boundaries and this is for educational and/or demonstration purpopes only. Eventually I would like to make this an automated script and maintain it to keep up to date. 

# Features like:

    - Docker compatibility (for easier deployment).

# Hardware (PC & VPS) 02/03/2026

# PC

    - Lenovo Legion Pro 7 16IRX8H
    - 13th Gen Intel Core i9 13900HX
    - Crucial 32 GB DDR5
    - NVidea 4080 GPU
    - Crucial 1 TB Nvme SSD

# Server

    - Hostinger
    - 2 vCores
    - 8 GB DDR5
    - 100 GB Nvme SSD
    

# Software (PC & VPS) 02/03/2026

# PC
    
    - Ms Win 11 H
    - Build 10.0.26200

# Server

    - Kali Linux 
 
# Instructions

{} = replace the variable with the CORRECT name and/or path
[] = commands in either Powershell or Linux CLI

# VPS

1. Get a VPS provider like Linode/OVH Cloud/Hostinger. Make sure the VPS can run a Kali Linux instance!

- 1.1 https://www.linode.com/ 
- 1.2 https://www.ovhcloud.com/en/
- 1.3 https://www.hostinger.com/

2. The basics 

- 2.1 Log in to your VPS instance.
- 2.2 Choose a Kali distro
- 2.3 Let the VPS install the distrubution
- OPTIONAL -
- 2.4 Make a backup of fresh server if not provdided

#  To do list (Server)

1.1 Log in to the server with SSH.

- 1.1  Windows Powershell: ssh -i {C:\User\{username}\.ssh\ed_25519.pub {username_server}@{ip_server}}
- 1.2  Linux CLI: ssh {username_server}@{ip_server}
- 1.3  When prompted for the password provide the password
- 1.4  Press return/enter
- 1.5  Check if CLI changed into {root$ip_server}
- 1.6  Linux CLI to check for root access: whoami
- 1.7  When you encounter issues look under # Troubleshooting


2. Change the default SSH (Secure Shell protocol) Linux CLI.

- 2.1  From you home/root directory you'll edit the file with a text editor of your preference: [sudo vim/nano /etc/ssh/ssh_config]
- 2.2  Linux CLI: ssh {username_server}@{ip_server}

3. Signing in with just an SSH key. No root password, defaulting to a SSH key is more secure. **Pro Tip:** Always test your key-based login in a separate terminal before disabling password authentication! Why 

4. Update the system.
   
- 4.1 sudo apt update && sudo apt upgrade && sudo apt autoremove -y
- 4.2 If prompted to install dependancies: y
- 4.3 press return/enter
- 4.4 reboot
- 4.5 log back into the server see 0.1/0.2
- 4.6 sudo ufw default allow outgoing
- 4.3  sudo ufw default allow outgoing
- 4.3  sudo ufw default allow outgoing

5. Configuring the ufw firewall.

- 5.1  sudo apt install ufw.
- 5.2  sudo ufw default deny incoming
- 5.3  sudo ufw default allow outgoing
- 5.4  sudo ufw allow {choose_a_port/tcp}
- 5.5  sudo ufw deny 80/tcp
- 5.6  sudo ufw deny 443/tcp
- 5.7  sudo ufw status verbose
- 5.8  sudo ufw default allow outgoing
- 5.9  sudo ufw default allow outgoing

6.  Default SSH port will have a honeypot. Instead of a Honeypot you can also install a tarpit.

7.  File logging.

8.  Bash update script that runs during off-peak hours.

9.  Bash configure script.

10.  Dependancies

- 10.1 Kali Linux (distribution)
- 10.2 vim
- 10.3 ufw
- 10.4 

11.  


# Script install instructions

1. Get a VPS or Local VM with a Kali Linux installation.

2. Download the server install script

# Troubelshooting



																					EOF
