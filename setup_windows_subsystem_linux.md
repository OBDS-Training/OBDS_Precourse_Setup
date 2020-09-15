# Windows Subsystem for Linux

## Installation

- In your web browser, navigate to <https://docs.microsoft.com/en-us/windows/wsl/install-win10>.
- Follow the instructions.
  The following sections provide additional details and advice to help you through the individual installation steps.

### Install the Windows Subsystem for Linux

When the instructions request to "Open PowerShell as Administrator":

- In the `Start Menu`, search for the `Windows PowerShell`. Don't click on it yet.
- Right-click on the `Windows PowerShell` icon, and click on `Run as administrator`.

Make sure you run the requested command, which should look like the following:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

### Update to WSL 2

Skip that section.
Do not update to WSL 2.

### Enable the 'Virtual Machine Platform' optional component

Skip that section.
Do not update to WSL 2.

### Set WSL 2 as your default version

Skip that section.
Do not update to WSL 2.

#### Install your Linux distribution of choice

Click on the Ubuntu distribution with the largest version number, which should look like the following:

```
Ubuntu 20.04 LTS
```

### Set up a new distribution

When prompted, type a Ubuntu username that will be yours when using the Linux subsystem.
For instance, this could be the username that was given to you on the cluster.

When prompted for a password, type something that is memorable to you, and secure enough if anyone gained access to your computer.

At this point, your Ubuntu terminal should display `Installation successful!` and a message that should look like

```
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

Welcome to Ubuntu 20.04.1 LTS (GNU/Linux 4.4.0-19041-Microsoft x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Tue Sep 15 10:45:36 BST 2020

  System load:    0.52      Processes:              7
  Usage of /home: unknown   Users logged in:        0
  Memory usage:   34%       IPv4 address for wifi0: 192.168.0.15
  Swap usage:     0%

1 update can be installed immediately.
0 of these updates are security updates.
To see these additional updates run: apt list --upgradable

The list of available updates is more than a week old.
To check for new updates run: sudo apt update


This message is shown once once a day. To disable it please create the
/home/kevin/.hushlogin file.
```

## Conclusion

You can continue using the Ubuntu terminal above for the current session.

You can also launch new Ubuntu terminals from the Windows `Start Menu` as follows:

- In the Windows Start Menu, search for `Ubuntu`.
- Click on the desired shortlisted menu item.

You can list distributions installed and available in your Windows Subsystem for Linux as follows:

- Open a Windows PowerShell console
- Type `wsl --list --verbose`
- You should see something like the following:

```
NAME              STATE           VERSION
* Ubuntu-20.04    Running         1
```
