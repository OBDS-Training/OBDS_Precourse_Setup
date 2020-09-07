# Logging into the CGAT Cluster


You will recieve a username and password for the CGAT high performance compute cluster by email. To access the cluster please open a terminal and type:
 
`ssh <username>@cgatui.imm.ox.ac.uk`

You will be asked to provide your password to gain access. To save typing passwords in the future we will set up a public-private key pair during the course.

Please note that cgatui is a login node only and has very limited compute capacity. Once you have logged in please continue to the head node:
 
`ssh cgath1`

You will be asked for your password again. 

Please use the passwd command to change your password when you log in:

`passwd`

When you first log in you will find yourself in your home directory /ifs/home/<username>. You can check you current directory using the print working directory command:

`pwd`

During the course we will work in the OBDS-training directory /ifs/obds-training/<cohort>/<username>. You can change to this directory / folder using the change directory command:

`cd /ifs/obds-training/<cohort>/<username>/`
 

