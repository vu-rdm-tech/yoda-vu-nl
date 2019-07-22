# Using the iRODS icommands

Since Yoda is based on [iRODS technology](https://www.irods.org), it is possible to transfer
data to and from Yoda using the iRODS communication protocol. 
This protocol supports very efficient transfer of large data files.

Researchers and data managers who are familiar with using commandline tools can optionally use the [iRODS icommands tools](https://docs.irods.org/master/icommands/user/).
Linux packages for these tools are available from [the iRODS package repository](https://packages.irods.org/).
After configuring your package manager to use the iRODS package repository, you will be able to install the _irods-icommands_ package.

## Configuration
The icommands tools require configuration parameters.  
These parameters are usually stored in a configuration file
named _~/.irods/irods\_environment.json_.

Please find the configuration per environment below:

| Environment          | Configuration | Remarks                  |
|:-------------------- |:------------|:-------------------------|
| Dynamics of Youth    | [Configuration](#dynamics-of-youth) | |
| Faculty of Geosciences | [Configuration](#faculty-of-geosciences) | |
| Faculty of Humanities  | [Configuration](#faculty-of-humanities) | Humanities researchers often use the _Institutions for Open Societies_ environment rather than this faculty environment. |
| Faculty of Science     |  [Configuration](#faculty-of-science)| |
| Faculty of Social and Behavioural Sciences | [Configuration](#faculty-of-social-and-behavioural-sciences) | |
| Faculty of Veterinary Medicine | [Configuration](#faculty-of-veterinary-medicine)| Also used by the Faculty of Medicine
| Institutions for Open Societies | [Configuration](#institutions-for-open-societies) | Also used by the Faculty of Law, Economics and Governance, as well as the Faculty of Humanities |
| University Corporate Offices    | [Configuration](#university-corporate-offices) | |

### Dynamics of Youth
Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "youth.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu1p/home",
    "irods_cwd": "/nluu1p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu1p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Geosciences

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "geo.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu11p/home",
    "irods_cwd": "/nluu11p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu11p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Humanities

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "gw.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu13p/home",
    "irods_cwd": "/nluu13p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu13p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Science

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "science.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu6p/home",
    "irods_cwd": "/nluu6p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu6p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Social and Behavioural Sciences

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "fsw.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu10p/home",
    "irods_cwd": "/nluu10p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu10p",
    "irods_authentication_scheme": "pam"
}
```

### Faculty of Veterinary Medicine

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "dgk.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc2",
    "irods_home": "/nluu9ot/home",
    "irods_cwd": "/nluu9ot/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu9ot",
    "irods_authentication_scheme": "pam"
}
```
Note that in the future we plan to change the default resource to _irodsResc_.

### Institutions for Open Societies

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "i-lab.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu5p/home",
    "irods_cwd": "/nluu5p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu5p",
    "irods_authentication_scheme": "pam"
}
```

### University Corporate Offices

Please cut and paste the below json information into your configuration file.
You will only need to change the example username to your Yoda username.
```
{
    "irods_host": "its.data.uu.nl",
    "irods_port": 1247,
    "irods_default_resource": "irodsResc",
    "irods_home": "/nluu12p/home",
    "irods_cwd": "/nluu12p/home",
    "irods_user_name": "exampleuser@uu.nl",
    "irods_zone_name": "nluu12p",
    "irods_authentication_scheme": "pam"
}
```
