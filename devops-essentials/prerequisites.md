Computer:
==========
Every device which handle all the complex tasks and gives result is a computer.
Ex: Mobile, Laptop, Desktop, Server, Smart Washing Machine, Smart AC etc.

Every IP enabled device is a computer

Computer has CPU, RAM, ROM, OS(Windows/Linux/MAC)

Linux is used in production servers because
1. Secure --> SSH
2. No graphics --> fast, low power, low bandwidth, low ram usage
3. Heavy performance
4. open source
5. can run for years no need to restart
6. no antivirus required

Unix/Linux follows same principles but unix is costly whereas linux not

MAC/Unix --> hardware and software are tightly coupled (we are buying both hardware and software)

Dell/HP servers --> we are buying only hardware not software (we can install any OS)

washing machine/routers --> comes with embedded linux

We can create linux OS with 10 or 12 MB and can install in any device (open source)

sensors, super computers everywhere linux can be installed

Client-Server Architecture:
============================
               request
client -----------------------> server
       <-----------------------
               response

Authentication Mechanisms:
---------------------------
1. What we can remember ex: username and password
2. What you have ex: RSA tokens, OTP Authenticator etc for high secure systems
3. What you are ex: fingerprints, retina, palm etc.

if any two mechanisms are enabled from above it is two-factor authetication

for linux servers we use 1 and 2

In linux, we call the second authentication mechanism as public and private key(ssh keys)

Private key is required to unlock the public key
ex: we have github.com and public key with this we cannot login to github server we need private key to unlock

By using mathematical algorithms we can generate public and private keys

command: ssh-keygen -f <file_name> --> it gives public and private key
ex: ssh-keygen -f avinash
        avinash --> private key
        avinash.pub --> public key
public key format:
ssh-ecdsa...(Algorithm)    AAC..(Key)     user@id(identity)

Firewall:
----------
Firewall controls the incoming traffic and outgoing traffic

incoming traffic --> inbound traffic(scan everything thats enters)
outgoing traffic --> outbound traffic (allow everyone to exit)

Ex: A person(incoming traffic) going into organisation(server) crossing security gate(firewall)
Few organisations like NASA, DRDO checks for both incoming and outgoing traffic

AWS:
-----

ec2-user will be created by aws by default

N.Virginia US-east-1 : use this region by default here the charges will be less for resources

Under AWS datacenters we have regions and under regions we have zones
Ex: Region(Hyderabad), Zones(Hydeast, Hydwest)
atleast 2 zones will be available if one zone is down traffic will be diverted to other

EC2 instance creation:
----------------------
Before creating instance create firewall and keys
firewall in AWS == security group
if outbound rule deleted no response from server
compute and storage gets charged
protocol --> set of rules(ex:http, https, RDP etc.)

To access windows server RDP connection(is a protocol based) is required

To access linux servers we need ssh protocol. To connect to linux server we need a ssh client (ex: putty, gitbash, mobaxterm etc..) these clients also uses ssh protocol at backend

\(back_slash) --> windows format
/(forward_slash) --> linux format

select t3.micro as ec2 instance type(low cost)

to connect to ec2 instance:
ssh -i <private_key> ec2-user@ip

While connecting to any server what it will ask??
1. which protocol
2. which port
3. which server
4. username and password

# if we stop the instance still we get charged because of data(Storage) inside of it so terminate the instance after usage

We need not to delete keypairs and security groups in aws they will not get charged

ec2 instance connection troubleshooting:
-----------------------------------------
1. file or directory not found - refer the key either by absolute or relative path
2. in security group check inbound and outbound rules - all traffic, all ports, source 0.0.0.0/0
3. keypair - while importing no newline