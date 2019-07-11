# Yoda for Faculty of Medicine
## iRODS protocol support
As Yoda is based on iRODS technology, high speed and restartable data
transfer is possible using the iRODS communication protocol. 
This protocol supports very efficient transfer of larger data files,
yet requires that the user is familiar with the Linux or Mac commandline
environment and commandline operations. 
The protocol is used by the iRODS icommand tools. More information on these
tools can be found on the 
[iRODS documentation website](https://docs.irods.org/master/). 

## Configuration
The iRODS protocol requires you to specify several communication parameters, for instance
the iRODS zone name and authentication method.
Typically these parameters are prepared and stored in a configuration file 
named `~/.irods/irods_environment.json`

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
Note that in the future we plan to change the default resource to `irodsResc`. 

