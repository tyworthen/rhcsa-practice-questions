# Create users and assign them to secondary groups

### Question:
* Create groups ***sysgrp*** 
* Create user **andrew** and **susan** who belong to this group (as secondary group)
* Create user **sarah** who does not have an access to the shell 
* Password for all the users should be **Postroll**

***
(scroll down for an answer)

<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

### Answer:

* The answer is pretty straightforward therefore I will provide just the commands: 

```
groupadd sysgrp

useradd andrew
useradd susan
useradd sarah -s /sbin/nologin

passwd andrew  # provide password for andrew
passwd susan   # provide password for susan
passwd sarah   # provide password for sarah

usermod -aG sysgrp andrew
usermod -aG sysgrp susan
```

* To make sure what groups the users belong to here are the commands:

```
id andrew
id susan
id sarah
```