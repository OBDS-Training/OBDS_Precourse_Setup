# Secure Shell Protocol (SSH) setup

The Center for Computational Biology (CCB)
at the MRC Weatherall Institute of Molecular Medicine (WIMM)
hosts a high-performance computing (HPC) cluster
that is available to all members of the University of Oxford
for scientific computing.

You can [read more](https://www.imm.ox.ac.uk/research/units-and-centres/mrc-wimm-centre-for-computational-biology/ccb-account) on the institute's website.

Before the start of the course, you must register for an account if you do not already have one. Please visit https://www.imm.ox.ac.uk/research/units-and-centres/mrc-wimm-centre-for-computational-biology/ccb-account/request-an-account then click on 'Apply for a full account' under the OBDS section and fill in the online form. Once your account has been created you will receive login credentials (a username and password). 

To log into the CCB HPC cluster:

- Connect to the University VPN.
- Open the `Terminal` application on your computer.
- Type the following, replacing `<username>` by your own username (without the `<>` symbols).

```
ssh <username>@cbrglogin2.molbiol.ox.ac.uk
```

- When prompted for your password, type it and press the `Return` key on your keyboard.

<details>
  <summary>When I type my password, why do characters not appear in the terminal?</summary>
  <b>Reason:</b>
  <p>
    For security reasons, when you type your password, the characters will not be displayed in the Terminal.
    This is normal, so that anyone looking over your shoulder while you type your password cannot read it.
  </p>
  <p>
    <b>Solutions:</b>
    <ul>
      <li>Option 1: If you are confident, type your password directly in the Terminal and press Enter when you are done.</li>
      <li>Option 2: If you are worried about mistyping your password, type you password in a text editor, then cut and paste it into the Terminal and press Enter.</li>
    </ul>
    <b>Tips:</b>
    <ul>
      <li>If you typed directly in the Terminal and you think you have made a mistake, keep the Delete key pressed for a few seconds, to delete everything you typed so far, and type your whole password from the start again.</li>
    </ul>
  </p>
</details>

[Next](microsoft_remote_desktop.md)
