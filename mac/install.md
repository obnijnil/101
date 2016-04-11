# Java

    Do not attempt to uninstall Java by removing the Java tools from /usr/bin. This directory is part of the system software and any changes will be reset by Apple the next time you perform an update of the OS.

* uninstall Java

```
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin 
sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefpane
```

* uninstall JDK

    JDK can be found in `/Library/Java/JavaVirtualMachines`.
```
rm -rf jdkmajor.minor.macro[_update].jd
```
