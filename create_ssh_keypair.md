# Create an SSH key pair

We will explain this in more detail during the course, suffice it to say that SSH key pairs simply represent another method of authentication that can be used when connecting to a remote server, as an alternative to a password.

An SSH key pair consists of two files:

1. A public key that is copied to the remote server - usually add to the file `~/.ssh/authorized_keys`.
2. A private key that is kept exclusively on the client computer that generated it.

Those two files are generated simultaneously on the client computer using the command `ssh-keygen`.

## MacOS

1. Open a terminal
2. Enter `ssh-keygen -t rsa -b 2048`.
   This command requests the RSA algorithm to generate a key 2048 bits long.
3. When prompted for a file path to save the key, do not type anything, and simply press the `Return` (also called `Enter`) key on your keyboard.
   This will save the key in the default location (typically, `~/.ssh/id_rsa`)
4. When prompted for a passphrase, choose whether:
    + You want to encrypt (i.e. protect) they key pair using a password of your choice.
      It is strongly recommended to do so, as this will be the last line of defence if someone gains access to your computer.
      With the right SSH configuration (see further below), this will allow you to connect the server without typing any password from your computer; while keeping your account protected by your original password for anyone (including you) connecting from another computer.
5. When prompted to enter the passphrase again, repeat the same action as your choice above.

At this point, the terminal will display some information about the key pair that was generated.
If you chose the default location as described above, you should see two new files:

- `~/.ssh/id_rsa`, the private key
- `~/.ssh/id_rsa.pub`, the public key

With those, it will be possible for you to use the key pair for logging into remote servers such as:

- The high performance computing cluster that we use for this course
- GitHub
- Other servers (e.g. a Raspberry Pi)

## Windows

### Method 1

1. Follow the instructions to [Install Atom and add-ons](atom_installation_instructions.md)
2. In the menu bar, click successively on `Packages` > `platformio-ide-terminal` > `New Terminal`, to launch a new terminal.
3. In the terminal, type `ssh-keygen.exe -t rsa -b 2048`.
4. Continue, following the MacOS instructions from point 3 onwards.

### Method 2

1. Download [PuTTYgen](https://www.puttygen.com/).
2. From the Start Menu, launch `PuTTYgen`.
3. In `Parameters`, select `RSA` and type `2048` for the number of bits.
4. Click on the `Generate` button.
5. Generate some randomness by moving your mouse cursor across the large grey rectangular area in the window.
6. When the key is ready, if you want to encrypt the key with a passphrase, fill the corresponding fields to set and confirm the passphrase.
  See the instructions for MacOS for more information to choose whether to set a passphrase.
7. Click on `Save public key` and `Save private key`.
   Save each key in a safe and memorable location for late use.
