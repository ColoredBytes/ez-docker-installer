<p align="center">
  <img src="./assets/images/github-header-image.png" alt="Header">
  <a href="https://github.com/ColoredBytes/Sempahore/blob/96113c308c5c5c57bb28591d058b2e90b2c65d33/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
  </a>
</p>

# :link: Table of Contents

- [:x: Problem](#x-problem)
- [:heavy\_check\_mark: Solution](#heavy_check_mark-solution)
- [:gear: Instructions](#gear-instructions)
- [:memo: Notes](#memo-notes)


## :x: Problem

I use docker for a lot of my Homelab and currently run it on Rocky Linux. Which works great BTW! The issue I had was that Dockers install script located [Here](https://get.docker.com/) currently does not have support for RHEL-like systesms minus [Fedora](https://docs.docker.com/engine/install/fedora/) and [RHEL](https://docs.docker.com/engine/install/rhel/) for s390x architecture.

## :heavy_check_mark: Solution

So I made this to make it easier on myself and perhaps others so we don't need to manually install all the time. 

## :gear: Instructions

- **Clone Repo.**
```bash
git clone https://github.com/ColoredBytes/Ez-Docker-Installer.git
```
- **Make the script executable.**
```bash
chmod +x Ez-Docker-Installer/install.sh
```
- **Run the script.**
 ```bash
 bash Ez-Docker-Installer/install.sh
```

## :memo: Notes
> [!NOTE]
> - You still need to add other users if you want them to run docker commands that can be done with.
>    - `sudo usermod -aG docker $USER`<br>
> - This script installs the CE Edition of both not Business. That needs to be upgraded manually.


