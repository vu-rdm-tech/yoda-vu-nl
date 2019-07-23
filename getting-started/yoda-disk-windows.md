# Connecting to the Yoda Network Disk on Windows

Look up the server address of your environment:

| Environment          | Server address | Remarks                  |
|:-------------------- |:------------|:-------------------------|
| Dynamics of Youth    | https://youth.data.uu.nl | |
| Faculty of Geosciences | https://geo.data.uu.nl | |
| Faculty of Humanities  | https://gw.data.uu.nl | Humanities researchers often use the _Institutions for Open Societies_ environment rather than this faculty environment. |
| Faculty of Science     | https://science.data.uu.nl | |
| Faculty of Social and Behavioural Sciences | https://fsw.data.uu.nl | |
| Faculty of Veterinary Medicine | https://dgk.data.uu.nl | Also used by the Faculty of Medicine
| Institutions for Open Societies | https://i-lab.data.uu.nl | Also used by the Faculty of Law, Economics and Governance, as well as the Faculty of Humanities |
| University Corporate Offices    | https://its.data.uu.nl   | |

## Mapping network drive

Open "This PC" from the Start menu

![alt text](screenshots/screenshot-windows-thispc.png "Screenshot Windows: This PC")

Open the Computer menu item and select "Map network drive". 

![alt text](screenshots/screenshot-windows-mapnwdrive.png "Screenshot Windows: Map network drive icon in This PC")
 
Select a drive letter - any free letter is okay. Now enter the server address of the environment in the Folder field (see table above).

![alt text](screenshots/screenshot-windows-connectfolder.png "Screenshot Windows: folder input field when mapping network drive")

Ensure the box "Connect using different credentials" is checked and click on the Finish button. 

![alt text](screenshots/screenshot-windows-connectdifcr.png "Screenshot Windows: checkbox for connecting using different credentials when mapping network drive")
 
Enter your user name and password. Tick the checkbox "Remember my credentials". Click on the "OK" button.

![alt text](screenshots/screenshot-windows-credentials.png "Screenshot Windows: dialog for entering credentials when mapping network drive")
 
The Explorer screen will show the folders you have access rights to. You
can now drag and drop your files to upload or download them.

## Alternative: use WinSCP

If you experience problems with accessing data using a mapped network drive, you can alternatively
use a different client program for accessing data in Yoda, such as [WinSCP](https://winscp.net).

First install WinSCP according to the [WinSCP install guide](https://winscp.net/eng/docs/guide_install).

Start WinSCP from the Desktop icon or the Start menu.

In the login window, ensure that the file protocol is set to "WebDAV" and encryption is set to "TLS/SSL implicit encryption".

![alt text](screenshots/screenshot-winscp-login-encsettings.png "Screenshot WinSCP: file protocol and encryption settings")

Enter the server address of your environment (see table above) in the Host name field. The port number should have its default value: 443.

![alt text](screenshots/screenshot-winscp-login-host.png "Screenshot WinSCP: host name setting")

Enter your user name and password. 

![alt text](screenshots/screenshot-winscp-login-credentials.png "Screenshot WinSCP: host name setting")

Click on the Save button and then on the Login button. WinSCP should now open your Yoda Drive.
