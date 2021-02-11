#  Question
You need to write all the steps with commands.<br />
1. Configure SSH using Public/Private Keys<br />
2. Configure SSH using username/password<br />
3. Change the default SSH server port<br />
4. Allow multiple users<br />
5. Deny specific user<br />
6. Allow some user to access only specific folder (TestFolder)

---

##  Answer:


+ #####SSH using public/private keys:


copy public/private key to remote machine and give below command<br />

`ssh username@ip_address`<br />

you log in remote server without enter password<br />


+ #####SSH using username/password :<br />

Go to usr/local/bin directory and create raza file<br />
 `sudo nano /usr/local/bin/raza`<br />
edit raza file, add some text username and ip address of raza<br />
  `ssh raza@ip_address`

Just enter username will login to remote remote machine <br />
 `raza`	
 </br />
 OR<br />
 if the public/private is not configured, then you enter password and login to remote machine<br />
<br />



+ #####Change the default SSH server port :<br />


Open the `/etc/ssh/sshd_config` file and add some line:<br />

Then, uncomment (Remove the leading # character) it and change the value with an appropriate port number (for example, 22000)<br />
`Port 22000`
<br />
 
<br />

 + #####Allow multiple users<br />



 go to `cd /etc/ssh/sshd_config` <br />
 add some this text at the end <br />
   `AllowUsers  user2 user3 user4` <br />

<br />

 + #####Deny specific user<br />

 go to `cd /etc/ssh/sshd_config` <br />


add some more text at the end <br />
   `DenyUsers user1 `

<br />

 + #####Allow some user to access only specific folder (TestFolder)<br />


add user raza and enter his password<br />

`adduser raza` <br />

set home directory for raza <br />

`sudo usermod  -d /var/testfolder/test  -m  raza` <br />
   
change folder permission (owner permission to raza)<br />

`chown -R raza:group test` <br />

if the you want that the folder of raza is read, write and execute by owner,groups and anyothers (as your choice)<br />

`chmod -R 777 test/`


---