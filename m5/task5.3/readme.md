# Task 5.3
## Part 1
1. Process in Linux can have 4 state:
    - Running - the process is either already running or ready to run and is waiting for CPU time to be given to it
    - Stoped - in this state of awaiting some event or release of a system resource.
    - Terminated - usually, processes that were stopped by a signal are in this state
    - Zombie - dead processes, they were stopped and are no longer running, but there is an entry in the process table for them, possibly due to the fact that there are child processes left
2. The `pstree` command. 

<img src="./screenshots/pstree.png" width="50%">

3. The /proc file system

> `/proc` - process information pseudo-filesystem


<img src="./screenshots/proc.png" width="50%">

<img src="./screenshots/proc_cmdline.png">

4. Information about processor

<img src="./screenshots/lscpu.png" width="50%">

5. The `ps` command information

<img src="./screenshots/ps_aux.png" width="50%">

6. Kernel and user process

> Kernel process have a PID from 1-999 and in ps information they display in `[]`

<img src="./screenshots/kernel_procces.png" width="50%">

> User process have a user and display like a commmon command

<img src="./screenshots/user_procces.png" >

7. List of process

<img src="./screenshots/stastus_proc.png" width="70%">

Status| Description
------|------------
R|running
D|waiting for writing
S|dont active
T|terminated
Z|zombie


8. Specific user process

<img src="./screenshots/vagrant_ps.png" width="80%">

9. Analyze tasks

<img src="./screenshots/vagrant_ps.png" width="80%">

> You can use ps with grep to filter and serching information

10. Top information display

<img src="./screenshots/top_with_filters.png" width="70%">

> Top dispay information about system workload  and information about processes

11. Top command user processes

<img src="./screenshots/top_user.png" width="80%">

12. Control top command

<img src="./screenshots/top_with_filters.png" width="50%">

> `top` allows to change priority of the process and kill the process.
> Also you can customize info using sort and filters

13. Sort content of the process by using %MEM

<img src="./screenshots/top_sort.png" width="80%">

14. `nice` and `renice` commands

<img src="./screenshots/renice_top_0.png" width="100%">

<img src="./screenshots/top_renice.png" width="1000%">

15. top change priority

<img src="./screenshots/nice_top.png" width="80%">

16. `kill` command 

<img src="./screenshots/kill_procces.png" width="700%">

> use `k` and set 6 or 9 signal 

Signal | Description
-------|-------------
1| Completion  
2| Interrupt
3| Quit
9| Kill
10| Bus error
11| Segmentation fault
15| Quit request
17| Stop
18| Stop signal sent from keyboard
19|Continue after stopping
28| Window change
30| User defined
31| User defined

17. `jobs` ,`fg` , `bg` and `nohup` commands

<img src="./screenshots/jobs_fg_bg.png" width="700%">

## Part 2

1. Use OpenSSH int the Windows 10

> to connect to the server use `ssh user@ip-adress -p 2222`

<img src="./screenshots/windows_open_ssh.png" width="50%">

> If you use pubkeyauthorization use ssh-agent service for seting private key

<img src="./screenshots/win_service_startup_type.png" width="50%">

> Add private key in ssh-agent base

<img src="./screenshots/add_private_ley.png" width="70%">
 
> Aslo can execute command and terminate session

<img src="./screenshots/ls%20from%20powershell.png" width="60%">

2. Set SSH on server

> configure sshd_config file for seting public key authorization and set 2222 port
and off PasswordAuthorization

<img src="./screenshots/sshd_config.png" width="70%">

<img src="./screenshots/disable_pasword.png">

> generate rsa keys 

<img src="./screenshots/key_gen_client.png" width="70%">

> copy rsa keys on a host 

<img src="./copy_id_rsa.png" width="50%">

> write rsa key in authorized_keys file

<img src="./screenshots/write_rsa.png" width="50%">

> connetcion by using putty

<img src="./screenshots/ubuntu_accsess.png" width="50%">

> connection by using openssh windows client

<img src="./screenshots/win_log_in.png" width="50%">

3. Keys for encryption SSH

> generate keys 

```
ssh-keygen -t rsa -b 2048
ssh-keygen -t edcsa -b 512
ssh-keygen -t ed25519 -b 512
```

<img src="./screenshots/key_gen_3.png" width="70%">

> copy keys on host

<img src="./screenshots/copy_pub_key.png" width="70%">

> rsa

<img src="./screenshots/write_rsa.png" >
<img src="./screenshots/connect_rsa.png" width="70%">

> ecdsa-sha2-nistp512

<img src="./screenshots/write_ecdsa.png" >
<img src="./screenshots/connect_ecdsa.png" width="70%">

> ed25519

<img src="./screenshots/write_ed.png" >
<img src="./screenshots/connect_ed.png" width="70%">

4. port-forwading

> set port forwarding in VB

<img src="./screenshots/port_forwading.png" width="70%">

> connect to the server

<img src="./screenshots/win_log_in.png" width="70%">

5. Traffic intercept 

> run tcpdump to intercept traffic and write in file

<img src="./screenshots/server_tcpdump.png">

> run ssh session

<img src="./screenshots/ssh_connect.png" width="90%">

> run telnet session

<img src="./screenshots/connect_telnet.png" width="50%">

> open data file in wireshark

<img src="./screenshots/wireshark_traffic.png" width="90%">

> explore telnet traffic 

<img src="./screenshots/telnet_password.png" width="80%">

> explore ssh traffic

<img src="./screenshots/ssh_traffic.png" width="90%">

> So we can say that dont recomend use telnet for remote connection 