This file goes through steps to check our atom installations are working as expect. 


# Using atom 

1) In your terminal make sure you are in your conda env of choice (e.g. obds-py3)

2) Navigate to the directory that you are using for your obds work using `cd` (if you need to make a new directory use `mkdir`

3) Open atom from the terminal by typing 
  
  `$ atom`
   
4) You should be greeted by the atom welcome screen -> if not see troubleshooting step 1 & 2 below

5) You can create a new file by pressing `ctr` + `n`
 
5) lets open a terminal in atom using the platformio-ide-terminal package that you previously installed.
 
 - at the bottom of your atom window there is a small icon that looks like `+` click on it will open a terminal windown with a little `[>_]` symbol next to the `+` - if you hover over the `[>_]` it will say `bash` - click on it and it will open at terminal window
 - you can also see a button for this terminal on the tool bar - if you hover over it it will say `toggle platformio-ide-terminal`. 

**IMPORTANT!! - Confusingly  there is another similar button to the platformio-ide-terminal in the tool-bar - if you hover over it it says `new terminal`. This terminal doesn't work - make sure you have opened a terminal using the above methods only!**
 
 8) Now lets check the path that ther platformio terminal is picking up.
 
 in the terminal within atom type the following 
 
 ``` 
     $ which python
```

The top line thats printed should contain the path to your conda installation and look something like this:
`/Users/charlie/miniconda/envs/obds-py3/lib/python3.8` 

If it's not don't worry we just need to do a couple more steps 
 
 9) Look at you $PATH variable that was printed 
 
 ```
     $ conda env list 
     $ echo $PATH
 ```
 
 - Is conda working?  
 - Note the position of your conda paths in the list of the $PATH variable - the order of the list is the order the places will be searched for python, if conda is at the end we need to set the platformio-terminal to add your conda path in front of the path that it is setting see troubleshooting 1 below. 
 

# Troubleshooting 

**1) When i'm in a terminal and type `atom` on the command line noting happens, even though I can open atom from lauchpad or my apps**

This is a problem that occurs because during the install of `atom` it requires the user to give `atom` permissions to allow you to use the `atom` command on the command line, in the atom installation [instructions](https://flight-manual.atom.io/getting-started/sections/installing-atom/) it states:

```
When you first open Atom, it will try to install the atom and apm commands for use in the terminal. 
In some cases, Atom might not be able to install these commands because it needs an administrator password. 
To check if Atom was able to install the atom command, for example, open a terminal window and type which atom. 
If the atom command has been installed, you'll see something like this:

 $ which atom
 /usr/local/bin/atom
 
 If the atom command wasn't installed, the `which` command won't return anything:

 To install the atom and apm commands, run "Window: Install Shell Commands" from the Command Palette,
 which will prompt you for an administrator password.
```

If this didn't happen during your install an alternative way to install the "Window Install Shell Commands" is to open atom by clicking on the icon. When atom opens on the top menu bar of the window where you have `file`, `edit`, `view` buttons etc click on the `Atom` menu button, then half way down there is a button that says `Install Shell Commands` - click on this and the shell commands will install (you might need to enter your laptop admin password).
Now open a freah terminal and try typing `atom` this time it should work

**2) How to open atom in a conda instance in Windows**

To open Atom in a specific conda enviroment on a windows machine - go to your menu and select the anaconda prompt - in the anaconda prompt activate the conda encironment that you want using `conda activate obds-py3`

then type `atom` to open your atom instance 

**3) the platformio ide does not pick up my conda python - its picking up the system python**
See fix here ->https://stackoverflow.com/questions/43207427/using-anaconda-environment-in-atom find 

In summary:

You can change the platformio-ide run script 
  
In this file `~/.atom/packages/platformio-ide-terminal/lib/platformio-ide-terminal.coffee`

change: 

```
        autoRunCommand:
          title: 'Auto Run Command'
          description: 'Command to run on terminal initialization.'
          type: 'string'
          default: ''
```
change to `default` to: 

```
        autoRunCommand:
          title: 'Auto Run Command'
          description: 'Command to run on terminal initialization.'
          type: 'string'
          default: 'export PATH=~/miniconda/envs/general/bin:/Users/charlie/miniconda/condabin:$PATH && conda activate base'
```
**Note that you need to export the path AND activate conda for the correct python to be picked up!**
https://stackoverflow.com/questions/43207427/using-anaconda-environment-in-atom


**4) even if i'm not in the obds conda env when i run a script in python using the `script` package its running in the obds env**

Check you have opened atom from the command line in the right environment

**5)I cannot see the big buttons at the top of the tool bar**
 
Make sure you have both the `tool-bar` and the `tool-bar-atom` packages installed in atom

**6) Set up atom with git and github**

- If you have file thats already in a git repository, click on it to open, then click on the github icon at the bottom of the `atom` window
- In the github pane you will see a 'log in to GitHub' panel, click on the `login` button
- this tells you you need to enter a token - click on the `github.atom.io/login` link to generate a token - it takens you to a browser page where you might need to put in yur github password and user name, once you've done this it should display a token that you can copy to your clipboard and then paste in the box in the atom github pane that says `Enter your token` - paste your token and click `login` - you atom is now linked to github for this repository 

**7) Can't remember my ftp-remote-edit password**

- go to file/config (mac) or edit/Config (ubuntu) - this will open up for .atom/config.cson file in atom (you might want to make a copy just incase you breaksomething) 
- delete the section relating to ftp-remote-edit and save e.g. 

```
  "ftp-remote-edit":
    config: "cdd0c9280bf92f67da37af1f0aba0821ad118cf8740169a88a868ed07a0fc"
    password: "fb97c97475f236c"

```
- restart atom - note you will need to set up your remote server details again  

**8) Change windows terminal to git bash within platformio-ide terminal**

        --> file -> settings -> packages -> type in platformio-ide-terminal
        --> go to settings of the package -> core section -> in shell override enter path to gitbash
        e.g. C:\Program Files\Git\bin\bash.exe
        
**9) I press the `+` to open a terminal in atom and all it prints is `chdir(2) failed.: No such file or directory`**

  - Is the document you currently have open you a document that is being shared by teletype?
  - Open a new file (`ctl` + `n`) and have this tab open and click on the '+' to open a new terminal - this should now open properly

  - why does this happen? Terminal opens in the directory the file you are using is it - if you try and open it while you have a teletype on the screen - it can't find this file location on your system - hence the `chdir(2) failed.: No such file or directory`

# Notes: 

Could change platformio-ide-terminal to atom-ide-terminal -> This needs testing

- The platformio terminal loads as new completely seperately from the environment that you open atom in - not sure at the moment how to configure this. maybe some flag from the bashrc to inherit properties of previous shell like we have for the cluster? 
