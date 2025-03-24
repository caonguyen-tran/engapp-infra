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
Install Docker and Docker Compose <br/>
After that, using shell script to fix error "permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied" <br/>
```
sudo usermod -a -G docker $USER
```
```
newgrp docker
```
