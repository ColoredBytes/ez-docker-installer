![Header](./assets/images/github-header-image.png)

# :link: Table of Contents

- [:x: Problem](#x-problem)
- [:heavy\_check\_mark: Solution](#heavy_check_mark-solution)
- [:gear: Instructions](#gear-instructions)
- [:memo: Notes](#memo-notes)
- [:balance\_scale: **LICENSE**](#balance_scale-license)


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
> - No need to run as sudo as that is handled in the script.
>    - Will prompt for Password if not run by root or the system is not configured for passwordless sudo.
> - You still need to add other users if you want them to run docker commands that can be done with.
>    - `sudo usermod -aG docker $USER`<br>
> - This script installs the CE Edition of both not Business. That needs to be upgraded manually.


## :balance_scale: **LICENSE**

```
MIT License

Copyright (c) 2024 Joshua Ross

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
