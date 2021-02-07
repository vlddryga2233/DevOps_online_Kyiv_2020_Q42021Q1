# Task 6.1 
 1. Create network

 > create VM1 with NAT and internal interfaces
 > create VM2 with internal interface


 2. Configure VM1

    > set ip adress for VM1 using netplan

    <img src="./screenshots/conf_network_vm1.png" width="50%">

    > enable NAT and configure  traffic forwading from VM2
 
    <img src="./screenshots/setting_forwading.png" width="50%">

    > Enable packet forwading

    <img src="./screenshots/enable_packet_forwading.png" width="50%">

    > Check configuration

    <img src="./screenshots/ifconfig_vm1.png" width="50%">


 3. Configure VM2

    > set ip adress for VM2 using netplan

    <img src="./screenshots/conf_network_vm2.png" width="50%">

    > check configuration

    <img src="./screenshots/ifconfig_vm2.png" width="50%">



 4. Check the route from VM to host

<img src="./screenshots/route_vm2_to_host.png" width="50%">


 5. Check access to the internet

<img src="./screenshots/check_internet_access.png" width="50%">


 6. Determine 8.8.8.8

 > 8.8.8.8 it is a google.dns

<img src="./screenshots/determine_8.8.8.8.png" width="50%">


 7. Determine ip address epam.com

<img src="./screenshots/ping_epam.png" width="50%">

 8. Determine default host gaateway and route table

> Route table

<img src="./screenshots/route_host.png" width="50%">

> Defatult gateway

<img src="./screenshots/host_gateway.png" width="50%">

 9. Trace the route google.com


<img src="./screenshots/traceroute_google.png" width="50%">