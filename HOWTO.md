# Création de la clé avec persistence

Boot the Live usb with persistence. Instructions for the Cinnamon desktop:

- disable autologin
System Settings > Login Window > Auto login > disable Automatic Login, disable Timed Login

- create a new user account
System Settings > Users and Groups > Add, Account Type Administrator, fill in Full name and Username, Add > Left clic user created, left click No password set to change password otherwise ecryptfs will not work.

- open a terminal to migrate the new user account to ecryptfs encryption, replace laurent with the username created:

Code: Select all

sudo ecryptfs-migrate-home -u laurent

Done :!:

Close your session and Log in as new user, home user files are now encrypted through ecryptfs.



