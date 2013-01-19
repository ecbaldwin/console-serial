console-serial
==============

Debian/Ubuntu package which automatically enables a login console on a serial port.

This package spins up getty to allow login on serial console on ttyS0.
Currently, it installs an upstart service that spins up getty on /dev/ttyS0.
Install it and it does the rest.

Many servers provide access to a virtual serial port that can be accessed over
a management network.  An example is the virtual serial port available in HP's
iLO.  Many VM hyper-visors also provide access to a virtual serial port in the
VMs.  For example, libvirt can be configured to allow access to a VM's serial
port by running "virsh console <domain>".

Serial ports are everywhere and they are indespensible for those of us who like
playing around with the network stack.  Spin up getty and make sure you have a
local user (not using LDAP or other network authentication service) and you
have a way to get yourself out of any mistakes you make while configuring the
network.
