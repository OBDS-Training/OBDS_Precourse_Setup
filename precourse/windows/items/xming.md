# XMing

XMing is an X window system that allows you display graphical output from a remote Linux server on your Windows 10 PC. 

- Open your browser and go to [https://sourceforge.net/projects/xming/](https://sourceforge.net/projects/xming/)
- Click on the green `Download` button. This will take you to a new page where download will start after a few seconds.
- Use Windows Explorer to find the downloaded .exe file and double-click to open the installer
- Follow the installation steps accepting the default options

## Testing your XMing install

- Open Git Bash
- Copy the following line to export the display parameter (we will explain this during the course)
  + export DISPLAY=localhost:0
- Connect to the CGAT cluster head node using X forwarding
  + ssh -XY username@cgatui.imm.ox.ac.uk
  + ssh -XY cgath2
- Type xeyes on the terminal. This should display a pair of eyes that follow your mouse around the screen.

[Next](r_setup_windows.md)
