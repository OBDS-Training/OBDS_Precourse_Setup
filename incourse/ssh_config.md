# Configuring SSH Shortcuts


Here, we configure a set of SSH profiles that allow you to connect more rapidly to the CCB cluster. Before you proceed, please make sure you have completed all the instructions for [Creating an SSH key pair](create_ssh_keypair.md).

## Windows 10

- Navigate to your home directory and enter the `.ssh` folder
- Create or open a file called `config` (without any extension!) in the `.ssh` folder using a text editor
- Add the following lines to the file.
  + N.B. Replace all occurences of `<username>` with yout CCB cluster username
```
Host *
    IdentityFile ~\.ssh\id_rsa
    User <username>
    Port 22
    Protocol 2
    TCPKeepAlive yes
    ServerAliveInterval 300
    ServerAliveCountMax 2
    ForwardX11 yes
    ForwardX11Trusted yes
    ForwardAgent yes
    Compression yes

Host ccb2
    Hostname cbrglogin2
    ProxyCommand ssh <username>@cbrglogin2.molbiol.ox.ac.uk nc %h %p
```
- Save the file (make sure that editor did not add any extension, the file name should be exactly `config`)


##  MacOS

Use the following template instead.

```
Host *
    IdentityFile ~/.ssh/id_rsa
    User <username>
    Port 22
    Protocol 2
    TCPKeepAlive yes
    ServerAliveInterval 300
    ServerAliveCountMax 2
    ForwardX11 yes
    ForwardX11Trusted yes
    ForwardAgent yes
    Compression yes
    XAuthLocation /opt/X11/bin/xauth
    AddKeysToAgent yes
    UseKeychain yes

Host ccb2
    Hostname cbrglogin2
    ProxyCommand ssh <username>@cbrglogin2.molbiol.ox.ac.uk nc %h %p
```

## Test your configuration

- Make sure you are connected to the University VPN.
- Open a terminal
- Type `ssh ccb2`. 
- You should log into the cluster and the prompt should start with `[username@cbrglogin2 ~]$`. Disconnect.
