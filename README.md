# Ez Docker Installer

### **Why you ask?**

Glad you Asked! I use docker for alot of my Homelab and currently run it on Rocky Linux. Which works great BTW! The issue I had was that Dockers install script located [Here](https://get.docker.com/) currently does not have support for RHEL like systesms minus [Fedora](https://docs.docker.com/engine/install/fedora/) and [RHEL](https://docs.docker.com/engine/install/rhel/) for s390x architecture. So I made this to make it easier on myself and perhaps others so we don't need to manually install all the time. 


### **Insttructions**
**Clone the repo.**
```
git clone https://github.com/Derp0ps/Ez-Docker-Installer.git`
```

**Make the script executable.**
```
cd Ez-Docker-Installer && chmod +x ez-docker-installer.sh
```

**Run the script.**
```
./ez-docker-installer.sh
```

**Navigate to Portainer if installed.**
- If you chose to Install portainer a link will spit out at the end like this `Portainer has been installed and is now running at https://127.0.0.1:9443`
    - Click the link make an account and Docker Away!

## Things to Know.
- No need to run as sudo as that is handled in the script. 
- You still need to add other users if you want them to run docker commands that can be done with a `sudo usermod -aG docker $USER`<br>
- This was tested on Debian 12, Ubuntu 22.04, Rocky Linux 9.3 and Alma Linux 9.3 and RHEL 9.3.
    - With that said it may work on earlier releases your mielage may vary. 
