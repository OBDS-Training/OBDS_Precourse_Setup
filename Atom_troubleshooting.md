This file goes through steps to check our atom installations are working as expect. 


Using atom 

1) In your terminal make sure you are in your conda env of choice (e.g. obds-py3)

2) Navigate to the directory that you are using for your obds work using `cd` (if you need to make a new directory use `mkdir`

3) Open atom from the terminal by typing 
  
  `$ atom`
  
4) You should be greated by the atom welcome screen 


5) Open atom_test.py in atom from the file/open menu 

6) run the atom_test.py in atom using the `run` button (looks like a 'play' button) at the top 

7) you will see that atom prints out your python path and version into a console - it should look something like this:

```
    Hi and welcome!!
    You are running a script to check you python path & version
    My python path is:
    /Users/charlie/Documents
    /Users/charlie/miniconda/envs/obds-py3/lib/python38.zip
    /Users/charlie/miniconda/envs/obds-py3/lib/python3.8
    /Users/charlie/miniconda/envs/obds-py3/lib/python3.8/lib-dynload
    /Users/charlie/miniconda/envs/obds-py3/lib/python3.8/site-packages
    My python version is:
    3.8.5 | packaged by conda-forge | (default, Sep 16 2020, 17:43:11) 
    [Clang 10.0.1 ]
    [Finished in 0.074s]
 ```
 
 7) lets open a terminal in atom using the platformio-ide-terminal package that you previously installed.
 
 - at the bottom of your atom window there is a small icon that looks like `[>_]` if you hover over it, it will say `bash` - click on it and it will open at terminal window
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
 
 
 
 
 
 
 
Q: I cannot see the big buttons at the top of the tool bar 
 
A: Make sure you have both the `tool-bar` and the `tool-bar-atom` packages installed


Wierd behavoirs 

- even if i'm not in the obds conda env when i run a script in python its running in the obds env 
- the platformio ide does not pick up my conda python - its picking up the system python 

