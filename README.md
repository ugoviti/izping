# izPing

## What is this?
izPing is a Multihomed Internet links tester, failover and recovery bash script for network balanced setups.
When called from izBalancing it automate the process of failover and recovery of connected Internet lines.

## Usage:
This script should not run standalone, but must be called from izbalancing script

## Requirements:
- GNU/Linux Firewall running Kernel >=2.6.10 (with iptables module CONNMARK available)
- Bash Shell >= 2.0
- Standard GNU/Linux coreutils utilities (cat, echo, grep, if, etc...)
- GNU Version of awk and sed utilities
- GNU/Linux Netfilter user space utilities (iptables >= 1.2.11)
- iproute2 utilities
- Two or more Internet connections
- An ethernet card for each ISP Router
- izBalancing configured and running (http://www.initzero.it/products/opensource/izbalancing)

## Installation:
- Download and configure izbalancing
- copy the izping script into /etc/rc./init.d/ and run:
```
   chmod 755 /etc/rc./init.d/izping
   chkconfig izping off
```
- edit the configuration variables inside izping script. Generally is needed to customize only MAILTO variable
- configure and start izbalancing, izping should start inside izbalancing
- look into logs if izping is running: tail -f /var/log/izping.log

