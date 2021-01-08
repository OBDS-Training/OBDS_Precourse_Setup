# Setup Checklist 

This page briefly summarises all the thngs that are set up prior and during the course along with some checks we need to make to make sure things are functioning correctly. 


## General 

- Github account
- Server account
- VPN setup
- Access to OBDS Github Repo
  - Cohort training repo
  - precourse set up instructions


## Server


- Linux
   - copy .bashrc & .inputrc
   - Add aliases
   - Create SSH Key (for GitHub access from server)
   - Add local laptop public key to .ssh/authorized_keys

- Conda 
  - install miniconda
  - install mamba
  - create obds_enviroment
  - modify .bashrc

- git 
  - installed
  - config
    - user name
    - email (github account)
    - default editor
  - enter rsa key on github
  - clone shared cohort repo from github
  - create own personal repo on github and locally


## Local Macos Machine

- NX -> set up connection to server
- FileZilla -> set up connection to server
- XCode - downloaded and installed - easiest to do this from app store

- Terminal
  - Create SSH key
  - copy public SSH key to server authorised_keys file
  - Create (copy) .ssh/config for tunnels to server

- Conda 
  - install miniconda
  - install mamba
  - create obds_enviroment
  - modify .bash_profile/.zshrc/.bashrc/.profile

- git 
  - installed (From Xcode)
  - config
    - user name
    - email (github account)
    - default editor
  - enter rsa key on github 
  - clone shared training cohort repo
  - clone own personal repo for the course
  
- Atom
  - install as app (don't install kite)
  - install packages
      - ftp-remote edit
      - platformio-ide-terminal
      - etc
  - open from the command line in conda env
  - can change conda env in terminal and pick up correct python 
  - path is set correctly in terminal 
  - modify terminal path/config file if nessecary
  - python IDE is working correctly and picking up conda python 
  - toolbar buttons are visable and working
  - debugger installed and working
  - link to github by adding token to github atom pane 
  - ftp-remote-edit working
  - start up no error messages


## Local Windows10 Machine

- NX -> set up connection to server
- FileZilla -> set up connection to server

- Bash terminal
  - Install git-bash (comes with git-scm)
  - Create SSH key
  - Copy public SSH key to server authorised_keys file
  - Create (copy) .ssh/config for tunnels to server

- git 
  - install git-scm
  - config
    - user name
    - email (github account)
    - default editor
  - enter rsa key on github
  - clone shared training cohort repo
  - clone own personal repo for the course
  
- Conda 
  - install miniconda
  - install mamba
  - create obds_enviroment
  - modify .bash_profile/.bashrc/.profile

- Atom
  - install as app (don't install kite)
  - install packages
      - ftp-remote edit
      - platformio-ide-terminal
      - etc
  - open from the command line in conda env
  - change the terminal to bash in platformio-ide-terminal settings
  - Ensure path is set correctly in terminal 
    - echo $PATH
    - which python
  - modify terminal path/config file if nessecary
  - python IDE is working correctly and picking up conda python - linter and autopep8 are working
  - toolbar buttons are visable and working
  - (debugger installed and working)
  - link to github by adding token to github atom pane 
  - ftp-remote-edit setup (week 3)
  - start up no error messages
