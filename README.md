# meta-das-base
Setup Yocto BSP sources and confiuration for met-das.

Followig are hardware requirements for the host to build bsp

- Must have atleast 12GB RAM and quad core.
- Must have atleast 150GB of free disk space.
- Should be running a stable version of Linux OS (Ubuntu 18.04 is preferred)

Install KAS on host

$ cd $HOME
$ git clone https://github.com/siemens/kas.git

Kas is written in Python3. We must install Python3, Pip3 and some Python packages.

$ sudo apt install python3 python3-pip
$ sudo pip3 install distro jsonschema kconfiglib PyYAML

Add $HOME/kas directory to PATH


For DAS4 SDK (ssh-dir is the path to ssh keys having access to meta-das)
$  kas-container --ssh-dir ~/.ssh build kas/das4_sdk.yml -c populate_sdk



