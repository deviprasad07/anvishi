---
layout: page
title: Monitor VM security in Openstack Cloud
permalink: /projects/monitor-vm-security-openstack-cloud/
exclude_from_nav: true
---
This was a study done for a course on Cloud computing. It involved the following goals:

* Established multi-node private cloud using OpenStack (Folsom version)
* Created and monitored victim and attacker VMs using Horizon (GUI component of OpenStack)
* Used attacker VM to simulate following attacks on victim VM
   - Denial of Service (DoS) attack using Slow HTTP Test
   - Denial of Service on SSL port 
   - Port probing using NMap (This is not a attack but the information exposed from this tool can be used in Black Hat Attack process i.e. to study system usage and behavior)
   - ARP Spoofing using Nemisis
* Used Nagios monitoring tool to detect DoS attack; and health of Glance, Keystone and Swift components of OpenStack.
* Our project was selected for future independent study by [Dr. I-Ling Yen](http://utdallas.edu/~ilyen/).