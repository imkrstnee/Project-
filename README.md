# Web Protection Project

## Objective

The purpose of the Web Protection Project is to create, secure and protect a cloud application utilizing SSL certificates and Microsoft Azure's security features. This hands-on experience was designed to deepen my understanding of network security and cryptography. 


### Skills Learned

- Access policy management
- Key vault component identification between keys, secrets, and certificates
- Creating a Web Application Firewawll policy (WAF) 

### Tools Used

- Microsoft Azure Portal used to map custom domain and create key vault
- Cloud Shell to use OpenSSL to generate self-signed certificates


### Steps

#### Part 1: Create an Azure Web App

1. Create Azure web application instance, back-end code, and service plan.
2. Assign unique IP to web app 

<img width="400" alt="Screenshot 2024-08-24 at 3 50 01 PM" src="https://github.com/user-attachments/assets/349677da-9d39-4ad7-b262-33d032677b68">


#### Part 2: Secure Web Application with SSL Certificates 

1. Create a key vault. After key vault has been created, it should encase the following information: keys, secrets, and certificates.

<img width="400" alt="Screenshot 2024-08-24 at 4 01 36 PM" src="https://github.com/user-attachments/assets/021a5b2b-7c63-4d4a-9699-c9e3cba38dda">

2. Create a self-signed certificate.

![Screenshot 2024-08-26 184016](https://github.com/user-attachments/assets/2fb0cd61-aebd-4582-98d5-8f3d51513a66)

2b. Things to note for the code above: 
- -x509: indicates for OpenSSL to create an SSL certificate
- -sha256: hashing algorithm
- -nodes: no DES (Data Encryption Standard) 
- -days 365: states the certificate will be valid for one year 
- -newkey rsa:2048: uses a 2048-bit RSA key
- -keyout cybertail.key: the output filename of private key
- -out cybertail_cert.crt: the ouput filename of certificate
- -addext "extendedKeyUsage=serverAuth": Indicates how a public key should be used, in this case server authentication

2c. Change to PFX format and download. 
![hi](https://github.com/user-attachments/assets/2c955dc7-6a01-4317-85f8-e418375bd29d)

3. Import and bind self-signed certificate to web app.

4. Import certificate to Key Vault

<img width="300" alt="3" src="https://github.com/user-attachments/assets/99725e0b-418d-4120-8606-d5daef988e93">

5. Import certificate to the App Service created prior in Part 1. 

<img width="300" alt="4" src="https://github.com/user-attachments/assets/9c886fcd-f67a-4c78-9f44-b51ee95acbfe">

6. Create and bind app service managed certificate.

#### Part 3: Protecting Web App with Azure's Security Features

1. Create a WAF (Web Application Firewall)
   
<img width="300" alt="5" src="https://github.com/user-attachments/assets/1ca3eb3e-eb1d-4d33-bb10-5cc3ad4a0904">

2. Manage WAF rules and configure custom WAF rules. 

<img width="300" alt="6" src="https://github.com/user-attachments/assets/ba864c23-8e10-4a08-9425-b64d25e0263c">

2b. The custom WAF entails if the Geolocation is not from the three countries listed in the rules, then deny traffic. 
