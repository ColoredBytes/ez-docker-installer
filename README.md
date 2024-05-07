# <div align="center"> Ez Docker Installer 🐳 </div>

### **Purpose**

Glad you Asked! I use docker for a lot of my Homelab and currently run it on Rocky Linux. Which works great BTW! The issue I had was that Dockers install script located [Here](https://get.docker.com/) currently does not have support for RHEL-like systesms minus [Fedora](https://docs.docker.com/engine/install/fedora/) and [RHEL](https://docs.docker.com/engine/install/rhel/) for s390x architecture. So I made this to make it easier on myself and perhaps others so we don't need to manually install all the time. 


### **Instructions**
- **Clone the repo.**
 ```
 git clone https://github.com/ross-jm/Ez-Docker-Installer.git
 ```

- **Make the script executable.**
 ```
 cd Ez-Docker-Installer && chmod +x ez-docker-installer.sh
 ```

- **Run the script.**
 ```
 ./ez-docker-installer.sh
 ```

**Navigate to Portainer if installed.**
- If you choose to Install Portainer a link will spit out at the end like this
> Portainer has been installed and is now running at https://127.0.0.1:9443`
    - Click the link make an account and Docker Away!

## Things to Know.
- No need to run as sudo as that is handled in the script.
    - Will prompt for Password if not run by root or the system is not configured for passwordless sudo.
- You still need to add other users if you want them to run docker commands that can be done with.
    - `sudo usermod -aG docker $USER`<br>
- This was tested on Debian 12, Ubuntu 22.04, Rocky Linux 9.3 Alma Linux 9.3, and RHEL 9.3.
    - With that said it may work on earlier releases your mileage may vary.
- This script installs the CE Edition of both not Business. That needs to be upgraded manually.
