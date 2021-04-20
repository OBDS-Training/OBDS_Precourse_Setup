# Log in the CCB cluster

The Center for Computational Biology (CCB)
at the MRC Weatherall Institute of Molecular Medicine (WIMM)
hosts a high-performance computing (HPC) cluster
that is available to all members of the University of Oxford
for scientific computing.

You can [read more](https://www.imm.ox.ac.uk/research/units-and-centres/mrc-wimm-centre-for-computational-biology/ccb-account) on the institute's website.

Before the start of the course, you must register for an account if you do not already have one. Please visit https://www.imm.ox.ac.uk/research/units-and-centres/mrc-wimm-centre-for-computational-biology/ccb-account/request-an-account then click on 'Apply for a full account' under the OBDS section and fillin the online form. Once your account has been created you will receive login credentials (a username and password). 

To log into the CCB HPC cluster:

- Connect to the University VPN.
- Open the `Terminal` application on your computer.
- Type the following, replacing `<username>` by your own username (without the `<>` symbols).

```
ssh <username>@cbrglogin2.molbiol.ox.ac.uk
```

- When prompted for your password, type it and press the `Return` key on your keyboard.

> For security reasons, when you type your password, the characters will not be displayed in the Terminal.
> This is normal.
>
> Tip:
>
> If you are worried about mistyping your password,
> Open a text editor, type your password there, then cut and paste it in the Terminal application.

[Next](microsoft_remote_desktop.md)
