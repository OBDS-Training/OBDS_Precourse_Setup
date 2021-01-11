# Configuring SSH

Before you proceed, please make sure you have completed all the instructions for [Creating an SSH key pair](create_ssh_keypair.md) and have the Atom text editor installed and configured.

Here, we configure a set of SSH profiles that allow you to connect more rapidly to the CGAT cluster.

## Windows 10

- Launch the `Atom` editor.
- In the `Atom` menu, click on `File`.
- Click on `Open Folder...`.
- Navigate to your home directory and select the `.ssh` folder.
- Click on `Select Folder`.
- Create or open a file called `config` (without any extension!) in the `.ssh` folder.
- Add the following lines to the file.
- N.B. Replace all occurences of `username` with yout CGAT cluster username
```
Host *
    IdentityFile ~\.ssh\id_rsa
    Port 22
    Protocol 2
    TCPKeepAlive yes
    ServerAliveInterval 300
    ServerAliveCountMax 2
    ForwardX11 yes
    ForwardX11Trusted yes
    ForwardAgent yes
    Compression yes

Host h2
    Hostname cgath2
    User <username>
    ProxyCommand C:\Windows\System32\OpenSSH\ssh.exe <username>@cgatui.imm.ox.ac.uk nc %h %p
```

- Save the file (make sure that editor did not add any extension, the file name should be exactly `config`)


##  MacOS

Use the following template instead.

```
Host *
    IdentityFile ~/.ssh/id_rsa
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

Host h2
    Hostname cgath2
    User <username>
    ProxyCommand ssh <username>@cgatui.imm.ox.ac.uk nc %h %p
```

## Test your configuration:
- Make sure you are connected to the University VPN.
- Open a terminal
- Type `ssh h2`. 
- You should log into the cluster and the prompt should start with `[username@cgath2 ~]$`. Disconnect.
