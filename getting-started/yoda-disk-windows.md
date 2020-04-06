# Connecting to the Yoda Network Disk on Windows

This website contains information about three methods for connecting to
the Yoda Network Disk on PCs and laptops that run Microsoft Windows:
- [YodaDrive](yoda-disk-yodadrive.md)
- The [Windows native WebDAV client](yoda-disk-windowsnative.md)
- [Cyberduck](yoda-disk-cyberduck.md)
- [WinSCP](yoda-disk-winscp.md)

Generally speaking, [YodaDrive](yoda-disk-yodadrive.md) is the preferred method. However, in some specific situations the [Windows native WebDAV client](yoda-disk-windowsnative.md) is a better alternative: 
- If you need to be able to connect to multiple Yoda environments simultaneously.
- If you can't install YodaDrive, for example if the security settings of your laptop
  prevent you from installing any new applications.
- YodaDrive is intended for use with Windows 10. If you use Windows 7 and are unable to upgrade,
  you can still use the native WebDAV client to connect to the Yoda Network Disk as a temporary workaround.

[WinSCP](yoda-disk-winscp.md) is an alternative for YodaDrive and the Windows native WebDAV client. The main difference
between the native
WebDAV client and YodaDrive on the one hand and WinSCP on the other hand, is that WinSCP is an application for working
with remote data, whereas the native WebDAV client and YodaDrive map the Yoda Network Disk to a drive transparently.
So you can use the native WebDAV client and YodaDrive to work with data in Yoda as if it was local data, but if you use 
WinSCP you may have to copy your data to a local disk or other network drive before being able to work with it, 
depending on the application and use case.

[Cyberduck](yoda-disk-cyberduck.md) Cyberduck like WinSCP is an application for working with remote data,
whereas WebDrive and YodaDrive map the Yoda Network Disk to a drive transparently. So you can use the WebDrive and 
YodaDrive to work with data in Yoda as if it was local data, but if you use
Cyberduck you may have to copy your data to a local disk or network drive before being able to work with it,
depending on the use case and application.