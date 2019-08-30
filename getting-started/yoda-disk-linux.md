# Connecting to the Yoda Network Disk on Linux

## Using GNOME Files

GNOME users can connect to the Yoda Network Disk with GNOME Files (also known as Nautilus in older versions of GNOME).

![alt text](screenshots/linux-connect-to-server.png "GNOME Files screenshot")

Click on "+Other Locations" and enter the server address in the "Connect to Server" bar.

| Environment          | Server address | Remarks                  |
|:-------------------- |:------------|:-------------------------|
| Dynamics of Youth    | davs://youth.data.uu.nl | |
| Faculty of Geosciences | davs://geo.data.uu.nl | |
| Faculty of Humanities  | davs://gw.data.uu.nl | Humanities researchers often use the _Institutions for Open Societies_ environment rather than this faculty environment. |
| Faculty of Law, Economics and Governance | davs://i-lab.data.uu.nl | |
| Faculty of Medicine    | davs://dgk.data.uu.nl | |
| Faculty of Science     | davs://science.data.uu.nl | |
| Faculty of Social and Behavioural Sciences | davs://fsw.data.uu.nl | |
| Faculty of Veterinary Medicine | davs://dgk.data.uu.nl | |
| Institutions for Open Societies | davs://i-lab.data.uu.nl | |
| University Corporate Offices    | davs://its.data.uu.nl  | |

Then click on the Connect button.

![alt text](screenshots/linux-enter-password.png "GNOME Files password dialog screenshot")

You will be prompted for a name and password. If you are an employee or student at Utrecht University, your user name is your Utrecht University email address and your password is your Solis password. Other users have usually received their user name and password via email. Click on the connect button.

## Using command line tools

If you prefer to use command line tools, you can use these methods:
- Mount the Yoda Network Disk as a davfs volume. You may need to install a davfs package on your system first. On Debian-based systems, such as Ubuntu: _apt install davfs2_, and answer "Yes" to the question about allowing regular users to mount WebDAV volumes. On RedHat-based systems, such as CentOS or Fedora: _yum install davfs2_. Now look up the server address of your environment in the table above.  Replace the "davs://" in the server address with "https://" when entering the mount command. For example: _mount -t davfs https://its.data.uu.nl /mnt_.
Important: Ensure that in the configuratiuon file /etc/davfs2/davfs2.conf the parameter "delay_upload" has the value 0 which may be different from the default. This avoids data flushing issues on larger file transfers. With credits to [Joost de Graaf](https://www.uu.nl/medewerkers/JdeGraaf) for reporting this solution.
- [The Cadaver commandline WebDAV client](http://www.webdav.org/cadaver/) is also compatible with the Yoda Network Disk.
