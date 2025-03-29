### Networking
* Networks can be as small as 2 computers connected at your home and as large as in a large company or connected systems worldwide known as Internet.
* Linux has a very strong set of networking instruments to provide and manage routing, bridging, virtual networks etc

#### LAN - Local Area Network
* LAN is a collection of devices connected together in one physical location 
* Each device has a unique IP address, with which the devices communicate with each other

#### IP - Internet Protocol
```
32 bit value 
1 bit = 1 or 0 
00000000 = 0 
11111111 = 255
```
* IP addresses can range from 0.0.0.0 to 255.255.255.255

#### Switch
* Sits within the LAN 
* Faciliates the connection between all the devices within the LAN

#### Router
* Sits between LAN and outside networks (WAN)
* WAN = Wide Area network 
* Connects devices on LAN and WAN 
* Allows networked devices to access the internet

#### Gateway
* IP address of router

#### Subnet
* Subnet is a logical subdivision of an IP network 
* Subnetting is the process of dividing a network into 2 or more networks 
* Devices in the LAN belong to same IP address range
* Example of IP address range: 
    1) Starting point of IP range, the first IP in the range 
    2) Sets the IP range 
* Value 255 fixates the Octet 
* Value 0 means free range

#### CIDR Block = Classless Inter-Domain Routing
* CIDR blocks are groups of addresses that share the same prefix and contain the same number of bits 
* Again subnet mask dictates how many bits are fixed 
* The CIDR notation is a shorthand way of writing this
* CIDR notation looks like this: 
    * /16 bits are fixed 
    * /24 bits are fixed

* Any device needs 3 pieces of data for communication:
    * IP Address
    * Subnet
    * Gateway

#### NAT = Network Address Translation
* NAT is a way to map multiple local private addresses to a public one before transferring the information 
* So if you make a request to the internet, the router replaces your private IP address with the router's IP
* Why? IP address within LAN are not visible to the outside network or internet, meaning they are private IPs. 
* This was necessary because there is only a limited number of IPv4 addresses available.
#### Benefits of NAT: 
* Security and protection of devices within LAN 
* Reuse IP addresses

#### Firewall
* A Firewall prevents unauthorized access from entering a private network 
* So by default, the server is not accessible from outside the LAN
* Using Firewall Rules you can define, which requests are allowed:
    * Which IP address in your network is accessible 
    * Which IP address can access your server 
    * For example: You can allow any device access your server

#### Port 
* Every device has a set of ports 
* Each port is unique on a device 
* You can allow specific ports (doors) 
* You can allow specific ports (doors) AND specific IP addresses (guests)
* For every application you need a port 
* Different applications listen on specific ports 
* There are many standard ports for many applications
    * Web servers: Port 80 
    * Mysql DB: Port 3306 
    * PostgreSQL DB: Port 5432 

#### DNS - Domain Name System
* Translates domain names to IP addresses 
* DNS is the phonebook of the internet 
* It translates human readable domain names (for example: www.amazon.com) to machine readable IP addresses
#### Domain Names
* Formed by the rules and procedures of the DNS 
* Domain names are organized in subordinate levels (subdomains) of the DNS root domain, which is nameless 
* The first-level set of domain names are the top-level domains (TLDs) 
* Below are the second-level and third-level domain names that are open for end-users
#### ICANN
* Manages the TLD development and architecture of the internet domain space 
* Authorizes Domain Name Registrars, which register and assign domain names 
#### How DNS resolution works
* When you enter a website in a browser, a DNS client on your computer needs to look up the corresponding IP address 
* It queries DNS servers to resolve the name 
* DNS queries can resolve in different ways 
* DNS Cache: A client can sometimes answer a query locally using cached (stored) information obtained from a previous query. Or the DNS server can use its own cache of resource record information to answer a query.
#### Request Flow
1. Name Server: Usually your Internet Service Provider 
2. Root Server: Requests for top level domains 
3. TLD Server: Stores the address information for top level domains 
4. Authoritative Name Server: Responsible for knowing everything about the domain, including IP address

#### Networking Commands
* Some useful networking commands to troubleshoot your network:
    * Ifconfig: Getting network configuration 
    * Netstat: Network connections, routing tables, interface statistics 
    * Ps aux: Tool to monitor processes running on your Linux system Query 
    * Nslookup: DNS lookup name 
    * Ping: Test network connection 

#### SSH- Secure Shell
* SSH or Secure Shell is a network protocol, that enables two computers to communicate securely 
* It protects the communications security and integrity with strong encryption
#### Use Case:
* Often used to "login" and perform tasks on remote computers, like installing software on a new server or to copy a file to the server
#### How it works:
* The protocol works in the client-server model 
* Meaning you use a program on your computer (ssh client) to connect to the remote server (SSH server) 
* For that you can use a graphical user interface, but mostly the CLI
#### 2 ways to authenticate
1. Username & Password 
    * Admin creates a user on the remote server 
    * User can then connect with the username and password 
2. SSH Key Pair 
    * Client creates a SSH Key Pair Key Pair = Private Key + Public Key 
    * Private Key = Secret key. Is stored securely on the client machine 
    * Public Key = Public. Can be shared, e.g. with the remote server
    * If public key of a person is not registered on the remote server, they cannot connect to it
#### SSH for Services:
* Services, like Jenkins, often need to connect to another server via SSH 
#### How to: 
* Create Jenkins User on application server 
* Create SSH key pair on Jenkins server 
* Add public key to authorized_keys on application server
#### Firewall and Port 22:
* SSH service (on SSH server) runs on port 22 
* That's why in firewall rule, we need to allow access on that port 
* But also configure the source (who can access the server on that port). Because SSH is powerful and needs to be restricted to specific IP addresses

* ssh UserName@SSHserver : Connect to a remote host
* ~/.ssh : .ssh under home directory is the default location for your ssh key pair
* known_hosts file: Lets the client authenticate the server to check that it isn't connecting to an impersonator 
* Authorized_keys file : Let's the server authenticate the user