# 🚀 Born2beroot

Born2beroot is a system administration project from 42 school. The project is designed to offer practical experience in setting up a virtual machine, installing a Linux-based operating system, and configuring it to meet a set of specific requirements.

![Born2beroot GIF](https://media.tenor.com/FHSANLwBWD4AAAAi/linux-linux-power.gif)

The project covers a range of system administration topics including partitioning, user management, permissions, sudoers rules, and basic shell scripting. It also emphasizes on the importance of security, requiring the implementation of several security measures such as setting up a strong password policy and using SELinux or AppArmor.

The end goal of the project is to have a fully functional and secure Linux server setup, providing a solid foundation for further exploration and learning in the field of system administration.

## 🎯 Features

- Linux server setup
- Strong password policy implementation
- Sudo rules setup
- And more...

## 🛠️ Installation and Setup

1. Download and install a virtual machine software (like VirtualBox).
2. Download the ISO image of the Linux distribution of your choice.
3. Create a new virtual machine and install the Linux distribution on it.
4. Follow the instructions in the project to set up the server and security rules.

## 📚 Step-by-step Guide

1. **Linux Server Setup**
	 - Install a Linux distribution on a server or a virtual machine. You can use a virtual machine software like VirtualBox or VMware.

2. **Strong Password Policy Implementation**
	 - Open the terminal and edit the PAM configuration file:
		 ```bash
		 sudo nano /etc/pam.d/common-password
		 ```
	 - Add the following line to enforce password complexity requirements:
		 ```bash
		 password        requisite                       pam_cracklib.so retry=3 minlen=8 difok=3 dcredit=-1 ucredit=-1 lcredit=-1 ocredit=-1
		 ```
	 - Save and close the file by pressing `Ctrl + X`, then `Y` to confirm saving, and finally `Enter` to confirm the file name.

3. **Sudo Rules Setup**
	 - Edit the sudoers file:
		 ```bash
		 sudo visudo
		 ```
	 - Add the following line to give your user sudo access:
		 ```bash
		 yourusername ALL=(ALL:ALL) ALL
		 ```
	 - Save and close the file by pressing `Ctrl + X`, then `Y` to confirm saving, and finally `Enter` to confirm the file name.

4. **SELinux or AppArmor Setup**
	 - Install SELinux or AppArmor. For example, to install SELinux on Debian, you can use:
		 ```bash
		 sudo apt-get install selinux-basics selinux-policy-default
		 ```
	 - Follow the instructions to set it up.

5. **User and Group Management**
	 - To add a new user:
		 ```bash
		 sudo adduser newusername
		 ```
	 - To add a new group:
		 ```bash
		 sudo groupadd newgroupname
		 ```
	 - To add a user to a group:
		 ```bash
		 sudo usermod -a -G groupname username
		 ```

6. **Partition Management**
	 - To list the partitions:
		 ```bash
		 lsblk
		 ```
	 - To create a new partition, you can use tools like `fdisk` or `parted`. Here's an example with `fdisk`:
		 ```bash
		 sudo fdisk /dev/sda
		 ```
	 - Follow the prompts to create a new partition.

7. **Basic Shell Scripting**
	 - Create a new shell script file:
		 ```bash
		 nano script.sh
		 ```
	 - Write your script. Here's a simple example:
		 ```bash
		 #!/bin/bash
		 echo "Hello, world!"
		 ```
	 - Save and close the file by pressing `Ctrl + X`, then `Y` to confirm saving, and finally `Enter` to confirm the file name.
	 - Make the script executable:
		 ```bash
		 chmod +x script.sh
		 ```
	 - Run the script:
		 ```bash
		 ./script.sh
		 ```

8. **System Monitoring**
	 - Install a system monitoring tool like `htop`:
		 ```bash
		 sudo apt-get install htop
		 ```
	 - Run the tool:
		 ```bash
		 htop
		 ```

9. **Scheduled Tasks Using Cron**
	 - Open the crontab file:
		 ```bash
		 crontab -e
		 ```
	 - Add a cron job. Here's an example that runs a script every day at 12:00:
		 ```bash
		 0 12 * * * /path/to/script.sh
		 ```
	 - Save and close the file by pressing `Ctrl + X`, then `Y` to confirm saving, and finally `Enter` to confirm the file name.

10. **System Logging**
		- System logs are usually located in `/var/log`. You can view them with tools like `less` or `tail`. For example, to view the syslog:
			```bash
			less /var/log/syslog
			```

11. **Network Configuration**
		- Network configuration can be done using the `ip` or `ifconfig` commands. For example, to view your network configuration:
			```bash
			ip addr show
			```

12. **Firewall Setup**
		- Install a firewall tool like `ufw`:
			```bash
			sudo apt-get install ufw
			```
		- Enable the firewall:
			```bash
			sudo ufw enable
			```
		- Add a firewall rule. For example, to allow SSH:
			```bash
			sudo ufw allow ssh
			```

> **Note:** Remember to replace `yourusername`, `newusername`, `newgroupname`, `groupname`, `username`, and `/path/to/script.sh` with your actual usernames, group names, and script paths.

## 🖥️ Usage

After setting up the server, you can access it through the terminal of your virtual machine software.

## 📝 Contributing

This project is a part of 42 school curriculum, contributions are not open.

## 📜 License

This project is licensed under the [MIT License](LICENSE).