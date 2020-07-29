# Updating your password for a mapped network drive on Windows

If you have changed your password and use [native WebDAV on a Windows system](yoda-disk-windowsnative.md),
you'll have to update your Yoda Network Drive configuration as well.

The instructions below assume that you have used
[the standard instructions to configure the Yoda Network Disk using native WebDAV](yoda-disk-windowsnative.md).
If you have configured the Yoda Network Disk in a different way, you might need to adapt the instructions
to your specific configuration.

## Instructions

First open the credential manager by clicking on the start button and typing &ldquo;Manage Windows Credentials&rdquo;.

![alt text](screenshots/windowsnative-managewincredentials.png "Screenshot: starting the Windows credential manager.")

Select the address of your Yoda Network Disk in the list of generic credentials. If you don't know the address, you can look it up in
the table in the [instructions for mapping the Yoda Network Disk](yoda-disk-windowsnative.md). 

![alt text](screenshots/windowsnative-managewincredentials-select.png "Screenshot: selecting the credentials of the Yoda Network Disk in the credential manager")

Choose &ldquo;Edit&rdquo;. Edit your credentials and click on the &ldquo;Save&rdquo; button.

![alt text](screenshots/windowsnative-managewincredentials-edit.png "Screenshot: editing the credentials of the Yoda Network Disk in the credential manager")

Restart your computer and open the mapped network drive in &ldquo;This PC&rdquo;.  You may have to
reenter your username and new password once more.

![alt text](screenshots/screenshot-windows-credentials.png "Screenshot Windows: dialog for entering credentials when mapping network drive")


