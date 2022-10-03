This is a work in project which uses Ansible templates to provision a simple 3 tiered network according to Cisco's high avaliability campus LAN guidelines, found [here](https://www.cisco.com/c/en/us/td/docs/solutions/Enterprise/Campus/HA_campus_DG/hacampusdg.html).

Because I'm hosting GNS3 on the same server I'm running Ansible on I have to use the cloud module to pass through Ansible's SSH connections. 

For the same reason I've also included routed links from dist1 to all the access etherswitches in order to manage them with Ansible instead of connecting all devices to a management switch. A switch installed between the cloud module and the GNS3 network caused frames to loop, indefinitely, between my server and the network, crashing GNS3.

![topology](https://i.imgur.com/UdM2Q37.png)
