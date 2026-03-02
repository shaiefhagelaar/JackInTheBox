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

#  To do list

0. Log in to the server with SSH.

     0.1  Windows Powershell: ssh -i {C:\User\{username}\.ssh\ed_25519.pub {username_server}@{ip_server}}
     0.2  Linux CLI: ssh {username_server}@{ip_server}
     0.3  When prompted for the password provide the password
     0.4  Press return/enter
     0.5  Check if CLI changed into {root$ip_server}
     0.6  Linux CLI to check for root access: whoami
     0.7  When you encounter issues look under # Troubleshooting


1. Change the default SSH (Secure Shell protocol) Linux CLI.

     1.1  From you home/root directory you'll edit the file with a text editor of your preference: [sudo vim/nano /etc/ssh/ssh_config]
     1.2  Linux CLI: ssh {username_server}@{ip_server}

2. Signing in with just an SSH key. No root password, defaulting to a SSH key is more secure. **Pro Tip:** Always test your key-based login in a separate terminal before disabling password authentication! Why 

3. Update the system.
   
     3.1 sudo apt update && sudo apt upgrade && sudo apt autoremove -y
     3.2 If prompted to install dependancies: y
     3.3 Press return/enter
     3.4 Reboot
     3.5 Log back into the server see 0.1/0.2
    
     4.3  sudo ufw default allow outgoing
    
     4.3  sudo ufw default allow outgoing
    
     4.3  sudo ufw default allow outgoing

4. Configuring the ufw firewall.
     4.1  sudo apt install ufw.
     4.2  sudo ufw default deny incoming
     4.3  sudo ufw default allow outgoing
     4.4  sudo ufw allow {choose_a_port/tcp}
     4.5  sudo ufw deny 80/tcp
     4.6  sudo ufw deny 443/tcp
     4.7  sudo ufw status verbose
     4.8  sudo ufw default allow outgoing
    
     4.3  sudo ufw default allow outgoing

5.  Default SSH port will have a honeypot. Instead of a Honeypot you can also install a tarpit.

6.  File logging.

7.  Bash update script that runs during off-peak hours.

7.  Bash configure script.

8.  Dependancies (


# Manual install instructions (Windows).

0. Get a VPS provider like Linode/OVH Cloud/Hostinger.

1. Log in to your VPS instance.

2.  

# Manual install instructions (Linux).

# Script install instructions

0. Get a VPS or Local VM with a Kali Linux installation.

1. Download the server install script

# Troubelshooting
