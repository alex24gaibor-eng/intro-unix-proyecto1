# Reflection

Digital security is not just technical; it also involves a responsible attitude. KeePassXC helps avoid errors
when creating strong passwords, and when combined with GNU Privacy Guard and hash verification, it protects 
the privacy and integrity of information. Together, these tools give us greater control over our data.

#Research questions

1. What is asymmetric encryption (public/private key) and how does it work in the context of GPG? What is the difference
between encrypting a message and digitally signing it?

Definition and Purpose: Asymmetric encryption (also known as public-key cryptography) is a type of encryption that
involves a mathematical relationship between two keys: a public key that is used for encrypting data and a private
key that is used for decrypting data. The key pairs in GPG comprise a public key, which may be shared with other people 
to allow them to send you secure messages; and your private key, which remains strictly secure on your device and allows 
you to read those encrypted messages.

Encryption vs digital signature:
Encryption: Encryption provides confidentiality. You use the recipient's public key to encrypt (i.e., scramble) a piece of
information so that only the recipient can decrypt (i.e., unscramble) it (i.e., read it).
Digital signature: A digital signature provides proof of authenticity and integrity. You use your own private key to sign a
message. The recipient can verify that you are indeed the originator of the message and that the message was not altered in 
transit by confirming that the message was signed using your public key.

2. Comparison of Email Services: Security and Privacy

This section compares ProtonMail, Gmail, and Outlook in terms of security and privacy features.
ProtonMail offers zero-access encryption at rest, meaning only the user can read their emails, while Gmail and Outlook use
standard encryption where Google and Microsoft hold the keys. All three services use TLS/SSL encryption in transit.
For end-to-end encryption (E2EE), ProtonMail includes it natively, whereas Gmail and Outlook require additional tools. 
In terms of privacy, ProtonMail follows a strict no-logs policy, while Gmail and Outlook may analyze data for functionality or profiling.
Finally, ProtonMail is based in Switzerland with strong privacy laws, while Gmail and Outlook operate under U.S. jurisdiction, making them
subject to government data access laws.

3. What is the PKI model based on Certificate Authorities (CA) and cite 2 advantages and 2 disadvantages compared to the Web of Trust?
Definition of PKI: A hierarchical model whereby a trusted third-party, referred to as the Certificate Authority (CA), verifies identities
and issues digital certificates.

Comparison:

Advantage #1: Global scalability is simplified (Web browsers automatically trust CAs).
Advantage #2: Centralized mechanism for revoking compromised certificates.
Disadvantage #1: Centralized failure point (If a CA is breached, all certificates are no longer valid).
Disadvantage #2: The cost to an organization usually includes paying a CA to verify and issue their digital certificate.

4. Investigate the EU's GDPR and Ecuador's LOPDP. What rights do they grant citizens regarding email and digital surveillance?

This section compares the rights granted to citizens under the General Data Protection Regulation (GDPR) and Ecuador’s Ley Orgánica
de Protección de Datos Personales (LOPDP), especially regarding email and digital surveillance.
Both regulations require clear and informed consent before processing personal email data, ensuring that users have control over how
their information is used. Regarding the right to erasure, GDPR allows individuals to request the deletion of all their personal data, 
including emails, while the LOPDP includes a similar right, enabling users to request data removal as established in its legal framework.
In terms of surveillance, both laws protect the privacy of communications. GDPR prohibits unauthorized interception of data, and the LOPDP 
treats communications as sensitive information, restricting arbitrary monitoring and reinforcing user privacy rights.

5. What is email metadata? Why doesn't content encryption protect it, and what are the implications for privacy?

Descriptoin: The metadata of an email includes the sender and recipient addresses, timestamps, subject lines, and IP addresses of the devices
used to send and receive the email, respectively.
How GPG Works: GPG allows users to encrypt only the body of the message while leaving the headers (metadata) in a readable format; this is 
necessary for mail servers to be able to determine how to deliver the email. 
Privacy Concerns: Even if the contents of an email are successfully encrypted, metadata has the potential to reveal social connections and patterns 
of behaviour, including professional networks, as well as provide just as much insight into a user's activities as the actual contents would.

