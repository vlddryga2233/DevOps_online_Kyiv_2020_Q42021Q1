# Module 2 Virtualization and Cloud basic # 

## Task 2.1  ##

## Part 1. Hypervisors ## 

1. The most popular hypervisors is VMware vSphere, Microsoft Hyper-V and  Citrix Xen 
2. VMware is using monolithic architecture that means implements a proprietary driver model within hypervisor.
MS Hyper-V is using mickrokernel architecture that simple partitioning and increasing relaibility and minimizes attack surface 

## Part 2. VirtualBox ##

1. Creating machine and installing ubuntu OS
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/2.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-12-15%20191706.png" width="50%">

2. Cloning machine and creating new group 
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/4.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/5.png" width="50%">

3. Creating snapshot tree
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/snapshots%20tree.png" width="50%">

4. Importing and exporting .ova file
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/6.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/7.png" width="50%">
5. Configuring virtual machine (usb, shared folder and network configurations)
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/10.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/9.png" width="50%">
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/8.png" width="50%">

6. Network modes

    Type | [Bridge](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/VM1_bridge.png) | [NAT](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/VM1_Nat.png) | VirtualHost [Adapter](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/vm-virtual_host_adapter.png) + [NAT](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/Vm2_host_adapter.png)
    -----|--------|-----|--------------------
    VM -> Inet | + |+ |         +
    VM -> host | - |+ |         +
    VM <-> host | - |- |        +
    VM <- host | + |- |         +
    VM1 <-> VM2 | + |- |        +

7. Working with CLI
    commands | results
    ---------|---------
      [cpu](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/working%20with%20CLI.png)    | [screen](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/modifyvm_memory_cpu.png)
      [memory](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/working%20with%20CLI.png) | [screen](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/modifyvm_memory_cpu.png)
      [create](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/working%20with%20CLI.png) | [screen](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/modifyvm_memory_cpu.png)
      [list](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/list.png)   |
      [snapshot](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/working%20with%20CLI.png)|[screen](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/modifyvm_memory_cpu.png)

## Part 3. Vagrant ##

1. Initializing environment and launching the box
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/vagrant3.png" width="50%">
2. Connecting to VM using Putty
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/ssh_putty.png" width="50%">

3. Stoping and destoying VM
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/vagrant3.png" width="50%">

4. Creating and configuring VM for vagrant
    - Seting su privelegion for vagrant user
    - Seting addition tools
    - Seting SSH key for remote access
5. Creating template for box
```
vagrant package --base 'server' --output server_template
```
6. Creating box
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-12-20%20163904.png" width="50%">
7. Initianolizing VMs
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-12-20%20172308.png" width="50%">
8. Connecting to VMs by Putty
<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m2/task2.1/screenshots/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-12-20%20172351.png" width="50%">