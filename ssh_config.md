# Configuring SSH

Before you proceed, please make sure you have completed all the instructions for [Creating an SSH key pair](create_ssh_keypair.md) and [Setting up Atom](atom_installation_instructions.md).

Here, we configure SSH profile that allowing you to connect more rapidly to the cluster for this course.

## Windows

- Launch the `Atom` editor.
- In the `Atom` menu, click on `File`.
- Click on `Open Folder...`.
- Navigate to your home directory and select the `.ssh` folder.
- Click on `Select Folder`.
- Create or open a file called `config` (without any extension!) in the `.ssh` folder.
- Add the following lines to the file.
  Replace all occurences of `username` by the username that was given to you on the cluster.

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

Host cgat
    Hostname cgatui.imm.ox.ac.uk
    User username
    IdentityFile ~\.ssh\id_rsa

Host h1
    Hostname cgath1
    User username
    IdentityFile ~\.ssh\id_rsa
    ProxyCommand C:\Windows\System32\OpenSSH\ssh.exe username@cgatui.imm.ox.ac.uk nc %h %p
```

- Save the file (make sure that editor did not add any extension, the file name should be exactly `config`)
- Test your configuration:
  + Make sure you are connected to the University VPN using `Cisco AnyConnect Mobility Client`.
  + In the `Atom` menu, click on `Packages`.
  + Select `platformio-ide-terminal` and `New Terminal`.
  + Type `ssh cgat`. You should log into the cluster and the prompt should start with `[username@cgatui ~]$`. Disconnect.
  + Type `ssh h1`. You should log into the cluster and the prompt should start with `[username@cgath1 ~]$`. Disconnect.

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

Host cgat
    Hostname cgatui.imm.ox.ac.uk
    User username

Host h1
    Hostname cgath1
    User username
    ProxyCommand ssh username@cgatui.imm.ox.ac.uk nc %h %p
```
