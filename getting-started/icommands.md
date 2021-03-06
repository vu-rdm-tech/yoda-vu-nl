# Getting started with the iRODS iCommands

Since Yoda is based on [iRODS technology](https://irods.org), it is possible to transfer
data to and from Yoda using the iRODS communication protocol. This protocol can be used
to transfer large amounts of data in an efficient way.

You will need to install client software that supports the iRODS protocol on your PC.
This page explains how to install and configure the iRODS iCommands. These
[command line tools](https://en.wikipedia.org/wiki/Command-line_interface) are the standard
implementation of an iRODS protocol client.

## Installing iRODS iCommands

Native iRODS iCommands packages are available for CentOS and Ubuntu.

Windows 10 users can run the iCommands in [the Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about).
MacOS users can run the commands inside a Linux VM.

### Installing iCommands on CentOS

iRODS currently supports CentOS 7. As of July 2021, CentOS 8 is not supported yet.

Use these commands to install the iCommands package on CentOS 7:

```
sudo yum -y install wget epel-release yum-plugin-versionlock
sudo rpm --import https://packages.irods.org/irods-signing-key.asc
wget -qO - https://packages.irods.org/renci-irods.yum.repo | sudo tee /etc/yum.repos.d/renci-irods.yum.repo
sudo yum -y install irods-runtime-4.2.9 irods-icommands-4.2.9
sudo yum versionlock irods-runtime irods-icommands
```

### Installing iCommands on Ubuntu

iRODS currently supports Ubuntu 18.04 LTS officially. Although Ubuntu 20.04 LTS is not supported officially,
 the iCommands work on this distribution.

Use these commands to install the iCommands package on Ubuntu 18.04 LTS:

```
wget -qO - https://packages.irods.org/irods-signing-key.asc | sudo apt-key add -
echo "deb [arch=amd64] https://packages.irods.org/apt/ bionic main" | sudo tee /etc/apt/sources.list.d/renci-irods.list
sudo apt update
sudo apt install irods-icommands
```

Ubuntu 20 will complain about missing some specific packages. If you need to use ubuntu 20 you can install the missing 
packages like this (versions as of June 2021): 
```
###
# 2. Install python-urlib3, python-requests and libssl1.0.0
wget -c  \
  http://security.ubuntu.com/ubuntu/pool/main/p/python-urllib3/python-urllib3_1.22-1ubuntu0.18.04.2_all.deb \
  http://security.ubuntu.com/ubuntu/pool/main/r/requests/python-requests_2.18.4-2ubuntu0.1_all.deb \
  http://security.ubuntu.com/ubuntu/pool/main/o/openssl1.0/libssl1.0.0_1.0.2n-1ubuntu5.6_amd64.deb
sudo apt install \
  ./python-urllib3_1.22-1ubuntu0.18.04.2_all.deb \
  ./python-requests_2.18.4-2ubuntu0.1_all.deb \
  ./libssl1.0.0_1.0.2n-1ubuntu5.6_amd64.deb
```


## Configuration

The iCommands need to be configured to connect to the right Yoda environment.

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "portal.yoda.vu.nl",
    "irods_port": 1247,
    "irods_home": "/tempZone/home",
    "irods_user_name": "xxx123",
    "irods_zone_name": "tempZone",
    "irods_authentication_scheme": "pam",
    "irods_encryption_algorithm": "AES-256-CBC",
    "irods_encryption_key_size": 32,
    "irods_encryption_num_hash_rounds": 16,
    "irods_encryption_salt_size": 8,
    "irods_client_server_negotiation": "request_server_negotiation"
}
```

## Getting started with using the iCommands

After installing and configuring the iCommands, you should be able to log in
on the Yoda environment using the [iinit command](https://docs.irods.org/master/icommands/user/#iinit).

Sections 5.3, 5.4 and 5.5 of the [iRODS beginner training](https://irods.org/uploads/2016/06/irods_beginner_training_2016.pdf)
contain some examples of how to use the iCommands to transfer and manage files. [The iCommands manual](https://docs.irods.org/master/icommands/user/)
has additional information.
