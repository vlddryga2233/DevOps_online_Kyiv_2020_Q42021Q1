# Task 5.2
1. Structure of the `/etc/passwd` and `/etc/group` file
> The `/etc/passwd` file keeps track of all users on the system.

> The structure of `/etc/passwd` file

> vlad : x : 1000 : 1000 : Vladyslav,420,06662860746,,Admin user : /home/vlad : /bin/bash

> Username : Password : UID : GID : GECOS : home directory : login shell

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/passwd%20file.png" width="50%">

> The `/etc/group` file contains the names of the groups present in Linux and lists the members of each group

> The structure of `/etc/group` file

> sudo : x : 27 : vagrant,vlad

> Groupname : Password : GID : Users

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/group%20file.png" width="50%">

> pseudo-users

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/pseudo-users.png" width="50%">

2. Structure of the UID

UID | defined
----|--------
0| root
1-999|system users
1000-65533| everything

> UID is the number assigned to each Linux user

```
usermod -u [uid] [username] // to change uid

id -u [username] // to define uid

cat /etc/passwd | grep [username] // to define uid

```

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/uid.png" width="50%">

3. Structure of the GID

> GID is a group identifier

> To define GID use following cmd
```
id -g [username]

cat /etc/group | grep [username]
```

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/gid.png" width="50%">

4. To determine belonging of user to the specific group check `/etc/group` file or use `id [sername]` command

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/uid%20and%20gid.png" width="50%">

5. Create user

> The most popular command for creating users is useradd and addusers

`sudo useradd -u [uid] -g [gid] -m (creare home dir) [username]`

`sudo adduser [username]`
 
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/useradd%20options.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/adduser%20keys.png" width="50%">


6. Change account name

`usermod -l [new name] [old name]`

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/change%20name.png" width="50%">


7. Skell directory

> The / etc / skel / directory is used to start the home directory when a user is first created.

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/skell_dir.png" width="50%">

8. Remove users 

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/userdel%20mail.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/delete_user.png" width="50%">

9. Lock and unlock users

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/lock_and_unlock_1.png" width="50%">

10. Remove user password

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/delete%20passwrd.png" width="50%">

11. Directory

> d|rwxrwxrwx | 2 | vlad | vlad | 4096 | Jan 19 12:07 | test

> type| file premission | hard links | owner | group | size | create date | name

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/ls.png" width="50%">

12.  Access rights

    > there are exitst 3 access rights: read write and execute. This rigts set for owner, group and for the others.

    > read      - r
      write     - w
      execute   - e

    

13. Each file has access rights for user, group and others. We can control who will use the file and how.

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/13.png" width="50%">

14. changing owner and access rights

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/chmod_chown.png" width="50%">

15. Representation of access rights

oct|bin|mask
---|---|----
0|000|---
1|001|--x
2|010|-w-
3|011|-wx
4|100|r--
5|101|r-x
6|110|rw-
7|111|rwx

```
chmod 744 == chmod rwxr--r--
``` 

> umask is a tool for setting right access for a new files which will be created

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/umask.png" width="50%">

16. Sticky bit

> Sticky bit don`t allow to delete file if you are not the owner

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/sticky-bit.png" width="50%">

17. Any scipt have to be executable

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m5/task5.2/screenshots/script_execute.png" width="50%">
