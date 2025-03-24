# engapp-infra
Infrastructure builder repository for engapp microservice. 
Services included:
- Kafka server
- Eureka server
- Mysql DB
- Mongo DB

Deploy to GCP by Docker compose:<br />
Using PuTTyGen to generate key pair: public key, private key<br />
Public key is saved in SSH keys (not a metadata) <br />

Install PuttyTools:<br />
```
apt-get install putty-tools
```
Convert PPK key to PEM key, using a shell pash:<br />
```
puttygen server.ppk -O private-openssh -o server.pem
```
Change permission for pem key: <br/>
```
sudo chmod 400 server.pem
```
SSH to VMs with a username is: public key name and External IP like the shell below: <br/>
```
sudo ssh -i server.pem <username:rsa-key-20250324>@<external_IP>
```
