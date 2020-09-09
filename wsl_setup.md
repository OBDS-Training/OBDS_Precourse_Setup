# Windows Subsystem for Linux (WSL) Setup

During the course we will need a local Linux terminal to connect to the high performance computing (HPC) cluster.
Windows 10 has the option to install a Linux subsystem that works well for this task.

If you do not have this installed already please follow these [instructions](https://www.windowscentral.com/install-windows-subsystem-linux-windows-10).
We recommend installing the Ubuntu distribution.

N.B. If you installed WSL using the Windows Store then your WSL home directory can be found at `C:\Users\[USERNAME]\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_[CODE]\LocalState\rootfs` on Windows File Explorer.
However, it is not advised to modify these files in Windows as it uses different encoding for line breaks.

Another useful trick is to type `explorer.exe .` in WSL and this will open Windows Explorer in the current directory.
