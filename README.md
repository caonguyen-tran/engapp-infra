# engapp-infra
Infrastructure builder repository for engapp microservice. 
Services included:
- Kafka server
- Eureka server
- Mysql DB
- Mongo DB

Deploy to GCP by Docker compose:
Using PuTTyGen to generate key pair: public key, private key
Public key is saved in SSH keys (not a metadata)
Install PuttyTools:
'''
apt-get install putty-tools
'''
Convert PPK key to PEM key, using a shell pash:
'''
puttygen server.ppk -O private-openssh -o server.pem
'''
