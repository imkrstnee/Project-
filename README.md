# Web Protection Project

## Objective

The purpose of the Web Protection Project is to build, secure and protect a cloud application utilizing SSL certificates and Microsoft Azure's security features. This hands-on experience was designed to deepen my understanding of network security and cryptography. 



### Skills Learned

- Cloud tenancy 
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

<img width="762" alt="Screenshot 2024-08-24 at 3 50 01 PM" src="https://github.com/user-attachments/assets/349677da-9d39-4ad7-b262-33d032677b68">


#### Part 2: Secure Web Application with SSL Certificates 

1. Create a key vault. After key vault has been created, it should encase the following information: keys, secrets, and certificates.

<img width="875" alt="Screenshot 2024-08-24 at 4 01 36 PM" src="https://github.com/user-attachments/assets/021a5b2b-7c63-4d4a-9699-c9e3cba38dda">

2. Create a self-signed certificate.




4. Important and bind self-signed certificate to web app.
5. Create and bind app service managed certificate. 
