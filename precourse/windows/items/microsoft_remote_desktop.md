# Microsoft Remote Desktop setup

We will use this program to open a virtual desktop
on the remote server that we use for this course.

The remote desktop will allow us to interact more easily with programs
that use a graphical user interfaces (GUI) running directly on the server.

Microsoft Remote Desktop is installed as part of Windows 10.

To set up a new RDP connection to the CCB cluster: 
- Open the Start menu and type “Remote”, then click “Remote Desktop Connection”
- Click the icon to launch the application
- Press ”Show Options” on the bottom left
- In the menu bar, click `+Add`, then `PCs`
- In `PC name:`, type `cbrglogin2.molbiol.ox.ac.uk`
- In `User account:`, select `+`
  + In `Username`, type the account username that you were given for the CCB server
  + In `Password`, type your account password for the CCB server
  + In `Display name`, type something memorable (e.g., OBDS account)
  + Click `Save` and you will return to the `Add a PC` screen
- In `Display name`, type something memorable, such as cbrglogin2
- Click `Save` and you should see a new thumbnail in the Microsoft Remote Desktop client,
alongside any other connection you might already have had.

To connect to the CCB cluster
- Double-click the new connection thumbnail
- The connection should take a few seconds to be established,
at which point the client should launch a full screen window
that presents you with a remote desktop session on the remote server.

Success!

[Next](filezilla.md)
