# How to SSH into the Rio

<https://docs.wpilib.org/en/stable/docs/software/roborio-info/roborio-ssh.html>

## **roboRIO User Accounts**

The roboRIO image contains a number of user accounts, but there are two of primary interest for FRC.

### **admin**

The “admin” account has root access to the system and can be used to manipulate OS files or settings. Teams should take caution when using this account as it allows for the modification of settings and files that may corrupt the operating system of the roboRIO. The credentials for this account are:

`Username: admin`

`Password:`

> ![NOTE] The password is intentionally left blank

## lvuser

The “lvuser” account is the account used to run user code for all three languages. The credentials for this account should not be changed. Teams may wish to use this account (via ssh or sftp) when working with the roboRIO to ensure that any files or settings changes are being made on the same account as their code will run under.

# Useful Roborio SSH commands

This command formats the system as an Unsorted Block Image fs
(Reimage the rio after running this)
`nisystemformat -f -t  ubifs && nisystemformat -f -t ubifs -c`
