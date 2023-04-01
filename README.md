# dhcp
DHCP implementation in PHP

`src/DHCP/` contains an implementation of DHCP protocol in PHP. It can be used to translate any DHCP packet from the 
network into PHP objects and vice versa.

`src/DHCPServer/` is a simple DHCP Server using the DHCP implementation, using MariaDb as a backend for storing
lease information. It also supports assigning static ip addresses to clients and was tested with default DHCP Clients
on Windows 7, MacOS Sierra and Red Hat Linux 7 (dhclient).
(Momchil) Will be tested on FreeBSD 13+

## Why?
(Momchil) Cause I need it for bHype
 
For more details and to see the code in action, check out our blog post: [mysteriouscode.io/blog/dhcp-implementation-in-php/](https://mysteriouscode.io/blog/dhcp-implementation-in-php/)

## Running DHCPServer

To start the server, run `php src/DHCPServer/server.php serve x.x.x.x/y`
Replace `x.x.x.x/y` with an IP and mask for the server (for example, 10.0.0.0/25)

## TODO
Remove dependencies on PSR and Symphony
Use MariaDb for a backend