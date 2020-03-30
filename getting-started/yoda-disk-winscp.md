# Connecting to the Yoda Network Disk on Windows Using WinSCP

Windows users can use [WinSCP](https://winscp.net) to access their data via the Yoda Network Disk,
as an alternative to the [native WebDAV client](yoda-disk-windowsnative.md) and
[YodaDrive](yoda-disk-yodadrive.md). The main difference between the native WebDAV client and YodaDrive
on the one hand and WinSCP on the other hand, is that WinSCP is an application for working with remote data,
whereas the native WebDAV client and YodaDrive map the Yoda Network Disk to a drive transparently. So you can
use the native WebDAV client and YodaDrive to work with data in Yoda as if it was local data, but if you use
WinSCP you may have to copy your data to a local disk or network drive before being able to work with it,
depending on the use case and application.

## Installing WinSCP 

The [WinSCP install guide](https://winscp.net/eng/docs/guide_install) explains how to install WinSCP.

## Using WinSCP

Start WinSCP from the Desktop icon or the Start menu.

In the login window, ensure that the file protocol is set to "WebDAV" and encryption is set to "TLS/SSL implicit encryption".

![alt text](screenshots/screenshot-winscp-login-encsettings.png "Screenshot WinSCP: file protocol and encryption settings")

Enter the server address of your environment (see table below) in the Host name field. The port number should have its default value: 443.

| Environment          | Server address | Remarks                  |   
|:-------------------- |:------------|:-------------------------|
| Dynamics of Youth    | https://youth.data.uu.nl | | 
| Faculty of Geosciences | https://geo.data.uu.nl | | 
| Faculty of Humanities  | https://gw.data.uu.nl | Humanities researchers often use the _Institutions for Open Societies_ environment rather than this faculty environment. |
| Faculty of Law, Economics and Governance | https://i-lab.data.uu.nl | | 
| Faculty of Medicine    | https://dgk.data.uu.nl | | 
| Faculty of Science     | https://science.data.uu.nl | | 
| Faculty of Social and Behavioural Sciences | https://fsw.data.uu.nl | | 
| Faculty of Veterinary Medicine | https://dgk.data.uu.nl | | 
| Institutions for Open Societies | https://i-lab.data.uu.nl | | 
| University Corporate Offices    | https://its.data.uu.nl   | | 
| SCOOP Consortium | https://scoop-disk.data.rug.nl | | 


![alt text](screenshots/screenshot-winscp-login-host.png "Screenshot WinSCP: host name setting")

You will be prompted for a name and password.
If you are an employee or student at Utrecht University, your user name is your Utrecht University email address (in lowercase) and your password
is your Solis password. External users have usually received their user name via email, along with a link to set their password.

![alt text](screenshots/screenshot-winscp-login-credentials.png "Screenshot WinSCP: host name setting")

Click on the Save button and then on the Login button. WinSCP should now open your Yoda Network Disk.
