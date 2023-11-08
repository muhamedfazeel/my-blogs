![MYSQL Logo](https://miro.medium.com/v2/resize:fit:1400/1*TTM5AleQfFJ-mItttJROdg.jpeg)

# Installation Guide

## Installing MySQL Community Server and Workbench

### Ref: The official guide.

1. **Download the MYSQL APT repository from [here](https://dev.mysql.com/downloads/repo/apt/)**.
2. **Install the deb package downloaded from the link above:**

> **sudo dpkg -i /PATH/version-specific-package-name.deb**

`Note: Server will start automatically after installation`

3. **Check the status of MySQL server:**
    > **systemctl status mysql**
4. **To switch to other major builds:**
    > **sudo dpkg-reconfigure mysql-apt-config**

> **sudo apt update** 5. **Install additional products and components:** > **sudo apt update**

> **sudo apt install <package-name>**

6. To install shared libraries:
    > **sudo apt-get install libmysqlclient21**

**`In case of any dependency issues`**

> **sudo apt install <dependency>**

# Uninstallation Guide

## Uninstalling MySQL Community Server and Workbench

1. **Stop MySQL:**

    > **sudo systemctl stop mysql**

2. **Remove all packages:**

    > sudo apt-get purge mysql-server mysql-client mysql-common mysql-server-core-_ mysql-client-core-_

3. **Remove configuration file:**

    > **sudo rm -rf /etc/mysql /var/lib/mysql**

4. **Remove unnecessary packages (optional):**

    > **sudo apt autoremove**

5. **Remove apt cache (optional):**
    > **sudo apt autoclean**
