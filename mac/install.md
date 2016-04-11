# Java

> Do not attempt to uninstall Java by removing the Java tools from /usr/bin. This directory is part of the system software and any changes will be reset by Apple the next time you perform an update of the OS.

* uninstall Java

```sh
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin 
sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefpane
```

* uninstall JDK

  JDK can be found in `/Library/Java/JavaVirtualMachines`.

```sh
rm -rf jdkmajor.minor.macro[_update].jd
```

* multiple JDKs

```sh
export JAVA_HOME_7=$(/usr/libexec/java_home -v1.7)
export JAVA_HOME_8=$(/usr/libexec/java_home -v1.8)
export JAVA_HOME=$JAVA_HOME_7
alias java7='export JAVA_HOME=$JAVA_HOME_7'
alias java8='export JAVA_HOME=$JAVA_HOME_8'
```
