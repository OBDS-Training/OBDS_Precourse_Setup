# Creating an SSH key pair

An SSH key pair simply represents another method of authentication that can be used when connecting to a remote server, as an alternative to a password. With the right SSH configuration (see further below), this will allow you to connect to the server from your computer without typing a password; while keeping your account protected by your original password for anyone (including you) connecting from another computer.

An SSH key pair consists of two files:

1. A public key that is copied to the remote server - usually add to the file `~/.ssh/authorized_keys` on the remote server.
2. A private key that is kept exclusively on the client computer that generated it and can only be accessed by a single user.

Those two files are generated simultaneously on the client computer using the command `ssh-keygen`.

## MacOS & Git Bash

1. Open a terminal
2. Enter `ssh-keygen -t rsa -b 2048`.
   This command requests the RSA algorithm to generate a key 2048 bits long.
3. When prompted for a file path to save the key, do not type anything, and simply press the `Return` (also called `Enter`) key on your keyboard.
   This will save the key in the default location (typically, `~/.ssh/id_rsa` & `~/.ssh/id_rsa.pub`)
4. When prompted for a passphrase, choose whether:
    + Keep it blank (more convenient but less secure)
    + You want to encrypt (i.e. protect) the key pair using a password of your choice. It is strongly recommended to do so, as this will be the last line of defence if someone gains access to your computer.
5. When prompted to enter the passphrase again, repeat the same action as your choice above.

At this point, the terminal will display some information about the key pair that was generated.
If you chose the default location as described above, you should see two new files:

- `~/.ssh/id_rsa`, the private key
- `~/.ssh/id_rsa.pub`, the public key

With those, it will be possible for you to use the key pair for logging into remote servers such as:

- The high performance computing cluster that we use for this course
- GitHub

# Adding an SSH Key to a remote server

- ssh-copy-id installs an SSH key on a server as an authorized key.
- `ssh-copy-id -i ~/.ssh/id_rsa <username>@cgatui.imm.ox.ac.uk`
- This logs into the server host, copies the key to the server, and configures it to grant access by adding them to the servers ~/.ssh/authorized_keys file. 
- This command will ask for your password for the server.
- Only the public key is copied to the server. The private key should never be copied to another machine.

## Testing the key

- `ssh -i ~/.ssh/id_rsa <username>@cgatui.imm.ox.ac.uk`
- The login should now complete without asking for a password. 
- Note, that the command might ask for the passphrase you specified for the key.

# Adding an SSH Key to your local SSH agent

We can stop the key from asking for it's password every time by adding the key to a local ssh agent.

- First we must start a local ssh agent
  + ``eval `ssh-agent -s` ``
- Next we add the key to the agent
  + `ssh-add`
  + You will be propmted for your ssh key password
- Now that the ssh key is added to the agent we should not be prompted for the passward again
  + `ssh -i ~/.ssh/id_rsa <username>@cgatui.imm.ox.ac.uk`
