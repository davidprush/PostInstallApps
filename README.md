# PostInstallApps

This is a Bash shell script to install apps after a fresh install of Ubuntu.

## Getting Started

To run the script make it executable and run it like any other Bash script.

``` sh
$ chmod +x PostInstallApps.sh
$ bash ./PostInstallApps.sh
```

### Prerequisites

Requires Ubuntu Linux.

### Default Apps

Default programs installed: top, nano, inxi, powertop, powerline, solaar, android-tools-adb, android-tools-fastboot, python-pip, git, python3-pip, npm, nodejs, pylint, ctags, screenfetch, youtube-dl, tlp, weechat, gtkhash, gparted, gcc, make.

Also installs Google Chrome and MS VSCode using the following:

``` sh
$ wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
$ sudo sh -c "echo "deb https://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list"
$ sudo apt-get update
$ sudo apt-get install google-chrome-stable
$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
$ sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EB3E94ADBE1229CF
$ sudo sh -c "echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list"
$ sudo apt-get update
$ sudo apt-get install code
```

## License

Do whatever you want with this...copy it...tell me it's horrible...edit it...whatever.