#### Example: How SSL Works for Amazon.com

1. Connecting to Amazon.com:

   1. When a user navigates to https://www.amazon.com, their browser initiates a secure connection to the Amazon server.

2. SSL Handshake:

   1. Client Hello: The browser sends a "Client Hello" message to Amazon's server, indicating it supports SSL/TLS and specifying its encryption preferences.

   2. Server Hello: Amazon's server responds with a "Server Hello" message, which includes its SSL certificate issued by DigiCert Inc. and the encryption algorithms it supports.

3. Certificate Exchange:

   1. SSL Certificate: Amazon’s server sends its SSL certificate to the browser. This certificate includes Amazon’s public key and details about the certificate authority (CA) — in this case, DigiCert Inc.
   2. Certificate Validation: The browser verifies the SSL certificate by checking that it is issued by a trusted CA (DigiCert Inc.) and that it is valid and not expired.

4. Encryption Setup:

   1. Pre-Master Secret: The browser generates a pre-master secret and encrypts it using Amazon’s public key from the SSL certificate. This encrypted pre-master secret is sent to the server.
   2. Session Keys: Both Amazon’s server and the browser use the pre-master secret to generate session keys. These keys will be used to encrypt and decrypt data during the session.

5. Secure Connection Established:

   1. Finished Messages: Both Amazon and the browser send "Finished" messages to confirm that the secure connection is established and that data encryption is active.

6. Visual Indicators:

   1. Padlock Icon: In the browser's address bar, users see a padlock icon, indicating that the connection is secure.

   2. HTTPS: The URL begins with https://, showing that the connection is encrypted.

#### Summary

When you visit https://www.amazon.com, Amazon’s server presents an SSL certificate issued by DigiCert Inc. During the SSL handshake, your browser verifies this certificate to ensure that Amazon is authentic. Once verified, a secure, encrypted connection is established, protecting any data exchanged between your browser and Amazon’s server. The padlock icon and https:// in the URL are visual indicators of this secure connection.
