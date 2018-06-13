# Retour WCF 2

## SOA

### Definition

Programming paradigm like object orientend programming or functionnal programming which consist in defining various webservices which interact with each others with messages.

A service-oriented architecture (SOA) is a style of software design where services are provided to the other components by application components, through a communication protocol over a network. The basic principles of service-oriented architecture are independent of vendors, products and technologies ( from Wikipedia)

### Micro service architecture

Software design
Each service has one particular function/purpose
They are all independant
This architecture faciliate the guarantee of the quality of service, by allowing to make their behaviour more predictable.

### Good practices

* Each webservice has to be a black box for it's consumers. 
* Self contained
* May consist of underlying services
* Specific income and outcome for each service

## Security on WCF services

To secure your WCF service, you can require the client to authenticate himself ( against an AD, using a certificate, etc ...) to secure the access to the functionality of the services.
![Image des security features WCF](https://www.tutorialspoint.com/wcf/images/wcf_security.jpg)
( https://www.tutorialspoint.com/wcf/wcf_security.htm )

We can secure the WCF services in two kind of way

### Secure the messages

Faster: The other way to secure is to encrypt the message, with a specific algorithm and the receiver will decrypt the job. You can also partially encrypt your message. 
For example you can only encrypt the content of the message, but let the header decrypted.

### Secure the transport layer

Cons: The main problem with securing the transport layer is that it only works on "point to point" connection. Because if you have another device beetween your client and your service, the message won't be encrypted on any router beetween the client and the server.

Pro: Faster

