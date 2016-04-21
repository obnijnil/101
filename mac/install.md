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

* [Java for OS X 2015-001](https://support.apple.com/kb/DL1572?viewlocale=en_US&locale=en_US)

  Java for OS X 2015-001 installs the legacy Java 6 runtime for OS X 10.11 El Capitan, OS X 10.10 Yosemite, OS X 10.9 Mavericks, OS X 10.8 Mountain Lion, and OS X 10.7 Lion.
  
  This package is exclusively intended for support of legacy software and installs the same deprecated version of Java 6 included in the 2014-001 and 2013-005 releases.

# Terminal

## Profile

There are [a bunch of color schemes](https://github.com/lysyi3m/osx-terminal-themes) available on GitHub for default Mac OS X Terminal.app.
