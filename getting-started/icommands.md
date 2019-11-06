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

iRODS currently supports CentOS 7. As of November 2019, CentOS 8 is not supported yet.

Use these commands to install the iCommands package on CentOS 7:

```
sudo yum -y install wget epel-release
sudo rpm --import https://packages.irods.org/irods-signing-key.asc
wget -qO - https://packages.irods.org/renci-irods.yum.repo | sudo tee /etc/yum.repos.d/renci-irods.yum.repo
sudo yum -y install irods-icommands
```

### Installing iCommands on Ubuntu

iRODS currently supports Ubuntu 16.04 LTS officially. Although Ubuntu 18.04 LTS is not supported officially,
as of November 2019, the iCommands work fine on this distribution.

Use these commands to install the iCommands package on Ubuntu 16.04 LTS or Ubuntu 18.04 LTS:

```
wget -qO - https://packages.irods.org/irods-signing-key.asc | sudo apt-key add -
echo "deb [arch=amd64] https://packages.irods.org/apt/ xenial main" | sudo tee /etc/apt/sources.list.d/renci-irods.list
sudo apt-get update
sudo apt -y install irods-icommands
```

## Configuration

The iCommands need to be configured to connect to the right Yoda environment.

Please find the configuration for each environment below:

| Environment          | Configuration | Remarks                  |
|:-------------------- |:------------|:-------------------------|
| Dynamics of Youth    | [Configuration](#dynamics-of-youth) | |
| Faculty of Geosciences | [Configuration](#faculty-of-geosciences) | |
| Faculty of Humanities  | [Configuration](#faculty-of-humanities) | Humanities researchers often use the _Institutions for Open Societies_ environment rather than this faculty environment. |
| Faculty of Law, Economics and Governance | [Configuration](#faculty-of-law-economics-and-governance)  | |
| Faculty of Medicine |  [Configuration](#faculty-of-medicine)| |
| Faculty of Science     |  [Configuration](#faculty-of-science)| |
| Faculty of Social and Behavioural Sciences | [Configuration](#faculty-of-social-and-behavioural-sciences) | |
| Faculty of Veterinary Medicine | [Configuration](#faculty-of-veterinary-medicine) | |
| Institutions for Open Societies | [Configuration](#institutions-for-open-societies) | |
| University Corporate Offices    | [Configuration](#university-corporate-offices) | |

### Dynamics of Youth
Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "youth.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu1p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu1p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Geosciences

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "geo.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu11p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu11p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Humanities

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "gw.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu13p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu13p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Law, Economics and Governance

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "i-lab.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu5p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu5p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Medicine

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.
```
{
    "irods_host": "dgk.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu9ot/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu9ot",
    "irods_authentication_scheme": "pam"
}
```
Note that in the future we plan to change the default resource to _irodsResc_.

### Faculty of Science

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "science.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu6p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu6p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Social and Behavioural Sciences

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "fsw.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu10p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu10p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Veterinary Medicine

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "dgk.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu9ot/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu9ot",
    "irods_authentication_scheme": "pam"
}
```

Note that in the future we plan to change the default resource to _irodsResc_.

### Institutions for Open Societies

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "i-lab.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu5p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu5p",
    "irods_authentication_scheme": "pam"
}
```

### University Corporate Offices

Please copy and paste this configuration into your
_~/.irods/irods\_environment.json_ configuration file.

You will need to change the example user name to your Yoda user name.

```
{
    "irods_host": "its.data.uu.nl",
    "irods_port": 1247,
    "irods_home": "/nluu12p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu12p",
    "irods_authentication_scheme": "pam"
}
```

## Getting started with using the iCommands

After installing and configuring the iCommands, you should be able to log in
on the Yoda environment using the [iinit command](https://docs.irods.org/master/icommands/user/#iinit).

Sections 5.3, 5.4 and 5.5 of the [iRODS beginner training](https://irods.org/uploads/2016/06/irods_beginner_training_2016.pdf)
contain some examples of how to use the iCommands to transfer and manage files. [The iCommands manual](https://docs.irods.org/master/icommands/user/)
has additional information.
