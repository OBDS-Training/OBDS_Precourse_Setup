# Setup Checklist 

This page briefly summarises all the thngs that are set up prior and during the course along with some checks we need to make to make sure things are functioning correctly. 


## General 

- Github account                    # Before course
- Server account                    # Before course
- VPN setup                         # Before course
- Access to OBDS Github Repo        # Before course
  - Cohort training repo            # Before course
  - precourse set up instructions   # Before course


## Server


- Linux
   - copy .bashrc & .inputrc                                # Week 1 - Day 1/2
   - Add aliases                                            # Week 1 - Day 1/2 
   - Create SSH Key (for GitHub access from server)         # Week 1 - Day 1/2
   - Add local laptop public key to .ssh/authorized_keys    # Week 1 - Day 1/2 

- Conda 
  - install miniconda             # Week1 - Conda Day
  - install mamba                 # Week1 - Conda Day
  - create obds_enviroment        # Week1 - Conda Day
  - modify .bashrc                # Week1 - Conda Day

- git 
  - installed                                         # Week1 - Git Day
  - config                                            # Week1 - Git Day
    - user name                                       # Week1 - Git Day
    - email (github account)                          # Week1 - Git Day
    - default editor                                  # Week1 - Git Day
  - enter rsa key on github                           # Week1 - Git Day
  - clone shared cohort repo from github              # Week1 - Git Day
  - create own personal repo on github and locally    # Week1 - Git Day


## Local Macos Machine

- NX -> set up connection to server
- filezilla -> set up connection to server
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
- filezilla -> set up connection to server

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
