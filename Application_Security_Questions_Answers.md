Encryption and Authentication


    * What is a three-way handshake?
---
The TCP handshake,TCP uses a three-way handshake to establish a reliable connection. 		The connection is full duplex, and both sides synchronize (SYN) and acknowledge (ACK) 	each other. The exchange of these four flags is performed in three steps—SYN,SYN-	ACK, and ACK

---
   * How do cookies work?

---
A cookie is a small bit of information that a website stores on your computer. When you revisit the website, your browser sends the information back to the site. Usually a cookie is designed to remember and tell a website some useful information about you.

---
    * How do sessions work?

---
Sessions are slightly different. Each user gets a session ID, which is sent back to the server for validation either by cookie or by GET variable.
Sessions are usually short-lived, which makes them ideal in saving temporary state between applications. Sessions also expire once the user closes the browser.

---

    * Explain how OAuth works.
---
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

---

    * What is a public key infrastructure flow and how would I diagram it?
---
Public Key Infrastructure is a complex subject, so you may be wondering if it actually performs encryption. The simple answer is yes, it does. What is PKI if not a one-stop-shop for the encryption of classified information and private identities?
PKI is best utilized for situations that require digital security, which is where encryption plays a vital role. PKI performs encryption directly through the keys that it generates. It works by using two different cryptographic keys: a public key and a private key. Whether these keys are public or private, they encrypt and decrypt secure data. 

By using a two-key encryption system, PKI secures sensitive electronic information as it is passed back and forth between two parties, and provides each party with a key to encrypt and decrypt the digital data.

Popular Ways PKI Security Is Used 

You might be thinking what PKI security might look like in your day to day. PKI security is used in many different ways. The main ways that PKI security can be used are:
- Securing emails
- Securing web communications (such as retail transactions)
- Digitally signing software
- Digitally signing applications
- Encrypting files
- Decrypting files
- Smart card authentication
---
   * What Is The Difference Between Public Key And Private Key?
---
The public key is available to any user that connects with the website. The private key is a unique key generated when a connection is made, and it is kept secret. 
When communicating, the client uses the public key to encrypt and decrypt, and the server uses the private key. This protects the user’s information from theft or tampering.

---
    * Describe the difference between synchronous and asynchronous encryption.

---
Synchronous Transmission	          
- In Synchronous transmission, Data is sent in form of blocks or frames.
- Synchronous transmission is fast.
- Synchronous transmission is costly.
- In Synchronous transmission, time interval of transmission is constant.
- In Synchronous transmission, There is no gap present between data.
- Efficient use of transmission line is done in synchronous transmission.
- Synchronous transmission needs precisely synchronized clocks for the information of new bytes.

Asynchronous Transmission
- In asynchronous transmission, Data is sent in form of byte or character.
- Asynchronous transmission is slow.
- Asynchronous transmission is economical.
- In asynchronous transmission, time interval of transmission is not constant, it is random.
- In asynchronous transmission, There is present gap between data.
- While in asynchronous transmission, transmission line remains empty during gap in character transmission.
- Asynchronous transmission have no need of synchronized clocks as parity bit is used in this transmission for information of new bytes.

---

    * Describe SSL handshake.
---
SSL Handshake
The following is a standard SSL handshake when RSA key exchange algorithm is used:

1.  Client Hello
Information that the server needs to communicate with the client using SSL. This includes the SSL version number, cipher settings, session-specific data.

2.  Server Hello
Information that the server needs to communicate with the client using SSL. This includes the SSL version number, cipher settings, session-specific data.

3.  Authentication and Pre-Master Secret
Client authenticates the server certificate. (e.g. Common Name / Date / Issuer) Client (depending on the cipher) creates the pre-master secret for the session, Encrypts with the server's public key and sends the encrypted pre-master secret to the server

4.  Decryption and Master Secret
Server uses its private key to decrypt the pre-master secret. Both Server and Client perform steps to generate the master secret with the agreed cipher.

5.  Encryption with Session Key
Both client and server exchange messages to inform that future messages will be encrypted.
---

    * How does HMAC work?
---
HMAC uses two passes of hash computation. The secret key is first used to derive two keys – inner and outer. The first pass of the algorithm produces an internal hash derived from the message and the inner key. The second pass produces the final HMAC code derived from the inner hash result and the outer key.

---
    * Why HMAC is designed in that way?

---
The design of the HMAC specification was motivated by the existence of attacks on more trivial mechanisms for combining a key with a hash function. For example, one might assume the same security that HMAC provides could be achieved with MAC = H(key || message).

---
    * What is the difference between authentication vs authorization name spaces?

---
Authentication and authorization might sound similar, but they are distinct security processes in the world of identity and access management (IAM).
Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.

- Authentication, in the form of a key. The lock on the door only grants access to someone with the correct key in much the same way that a system only grants access to users who have the correct credentials.

- Authorization, in the form of permissions. Once inside, the person has the authorization to access the kitchen and open the cupboard that holds the pet food. The person may not have permission to go into the bedroom for a quick nap. 
---

    * What’s the difference between Diffie-Hellman and RSA?
---
RSA and the Diffie-Hellman Key Exchange serve as the foundation for the security we use today. However, the two technologies differ dramatically. The Diffie-Hellman approach has each party generate both a public and private key, but only the public key is shared. Once the client on either end of the transaction has verified the other person’s public key, the exchange can be shared.

Because the Diffie-Hellman Key Exchange doesn’t authenticate either party, a hacker could more easily send spoof messages posing as one of the parties in the transaction. For this reason, the Diffie-Hellman approach requires an additional digital signature component. Both RSA and the Diffie-Hellman Exchange have their merits, with technology professionals commonly choosing one over the other due to their own personal preferences. RSA permits digital signatures, a key differentiator from the Diffie-Hellman approach.

Although both the Diffie-Hellman Key Exchange and RSA are the most popular encryption algorithms, RSA tends to be more popular for securing information on the internet. Still, cryptography varies from one site to the next, so you probably encounter a combination of both types throughout a given day without even realizing it.

---

    * How does Kerberos work?
---
Kerberos is a computer network security protocol that authenticates service requests between two or more trusted hosts across an untrusted network, like the internet. It uses secret-key cryptography and a trusted third party for authenticating client-server applications and verifying users' identities.

---
     * Kerberos Protocol Flow Overview

---
Let's take a more detailed look at what Kerberos authentication is and how it works by breaking it down into its core components.
Here are the principal entities involved in the typical Kerberos workflow:

Client. The client acts on behalf of the user and initiates communication for a service request
Server. The server hosts the service the user wants to access
Authentication Server (AS). The AS performs the desired client authentication. If the authentication happens successfully, the AS issues the client a ticket called TGT (Ticket Granting Ticket). This ticket assures the other servers that the client is authenticated
Key Distribution Center (KDC). In a Kerberos environment, the authentication server logically separated into three parts: A database (db), the Authentication Server (AS), and the Ticket Granting Server (TGS). These three parts, in turn, exist in a single server called the Key Distribution Center
Ticket Granting Server (TGS). The TGS is an application server that issues service tickets as a service
Now let's break down the protocol flow.
First, there are three crucial secret keys involved in the Kerberos flow. There are unique secret keys for the client/user, the TGS, and the server shared with the AS.
Client/user. Hash derived from the user's password
TGS secret key. Hash of the password employed in determining the TGS
Server secret key. Hash of the password used to determine the server providing the service.
The protocol flow consists of the following steps:

Step 1: Initial client authentication request. The user asks for a Ticket Granting Ticket (TGT) from the authentication server (AS). This request includes the client ID.

Step 2: KDC verifies the client's credentials. The AS checks the database for the client and TGS's availability. If the AS finds both values, it generates a client/user secret key, employing the user's password hash.
The AS then computes the TGS secret key and creates a session key (SK1) encrypted by the client/user secret key. The AS then generates a TGT containing the client ID, client network address, timestamp, lifetime, and SK1. The TGS secret key then encrypts the ticket.

Step 3: The client decrypts the message. The client uses the client/user secret key to decrypt the message and extract the SK1 and TGT, generating the authenticator that validates the client's TGS.

Step 4: The client uses TGT to request access. The client requests a ticket from the server offering the service by sending the extracted TGT and the created authenticator to TGS.

Step 5: The KDC creates a ticket for the file server. The TGS then uses the TGS secret key to decrypt the TGT received from the client and extracts the SK1. The TGS decrypts the authenticator and checks to see if it matches the client ID and client network address. The TGS also uses the extracted timestamp to make sure the TGT hasn't expired.

If the process conducts all the checks successfully, then the KDC generates a service session key (SK2) that is shared between the client and the target server.

Finally, the KDC creates a service ticket that includes the client id, client network address, timestamp, and SK2. This ticket is then encrypted with the server's secret key obtained from the db. The client receives a message containing the service ticket and the SK2, all encrypted with SK1.

Step 6: The client uses the file ticket to authenticate. The client decrypts the message using SK1 and extracts SK2. This process generates a new authenticator containing the client network address, client ID, and timestamp, encrypted with SK2, and sends it and the service ticket to the target server.

Step 7: The target server receives decryption and authentication.  The target server uses the server's secret key to decrypt the service ticket and extract the SK2. The server uses SK2 to decrypt the authenticator, performing checks to make sure the client ID and client network address from the authenticator and the service ticket match. The server also checks the service ticket to see if it's expired.

Once the checks are met, the target server sends the client a message verifying that the client and the server have authenticated each other. The user can now engage in a secure session.After coming so far in learning what Kerberos is, let us next look into the topic if Kerberos is infallible.

---

    * If you're going to compress and encrypt a file, which do you do first and why?
---

Compress first. Once you encrypt the file you will generate a stream of random data, which will be not be compressible. The compression process depends on finding compressible patterns in the data.

---

    * What is the difference between encryption and encoding?
---
Encoding is for maintaining data usability and can be reversed by employing the same algorithm that encoded the content, i.e. no key is used. Encryption is for maintaining data confidentiality and requires the use of a key (kept secret) in order to return to plaintext.

---

    * What is the difference between 128 and 256?
---
A bigger key always holds a better chance of remaining secure. Using AES with 256 bit keys enhances the number of AES rounds that need to be done for each data block such as it takes 10 rounds for 128-bit and 14 rounds for 256-bit encryption.
It adds an extra layer of security for users. Username and password will be safe with 256-bit encryption. The speed issue for ISP will be solved with 256-bit encryption.

---

    * How do I authenticate you and know you sent the message?
---

---

    * Should you encrypt all data at rest?
---
Encrypting data at rest protects the organization from the physical theft of the file system storage devices (which is why end-user mobile devices from laptops to cell phones should always be encrypted).
Encrypting the storage subsystem can protect against such attacks.

---

#### source: questions from tadwhitakers Security_Engineer_Interview_Questions (github repo)
###  Check out the updated list https://gist.github.com/mafiaguy/dae5648a260b8eb9ace22369a68132af
