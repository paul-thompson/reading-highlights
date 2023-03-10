# Debunking Myths About HTTPS   Jmau111

**Author:** Don’t trust the padlock  
**Full title:** Debunking Myths About HTTPS | Jmau111  
**URL:** https://blog.julien-maury.dev/en/snippets/https-myths/  
**Source:** #articles #instapaper #readwise

- HTTPS implements TLS (Transport Layer Security) for the HTTP protocol. 
   
- The idea with TLS is to prevent the data from being sent in plain text (like in HTTP), allowing attackers to read it if they manage to intercept the requests 
   
- TLS secures communications with cryptographic keys, so theoretically, even if someone manages to intercept the requests (e.g., Man-In-The-Middle attacks), the data will be impossible to exploit 
   
- Researchers and cybercriminals have found various angles of attack to spoof identities and impersonate the TLS client 
   
- Hosting services often provide SSL certificates for free (e.g., Let’s encrypt) or for a specific fee. 
   
- Certificates are delivered by a certificate authority (CA) that is independent from hosting providers, but these services usually handle the installation and activation for their customers 
   
- A website can also have a self-signed certificate that is not verified by any official authority (CA), but it will be likely flagged as “not secure” by the browser. 
   
- The lock icon may give a false impression of security, as cybercriminals can obtain legitimate SSL certificates for typo-squatting domains too. Indeed, most phishing and scamming websites are HTTPS. 
   
- it’s possible to act as a proxy under certain conditions without any knowledge from the victims who wouldn’t change their behavior, as nothing would look wrong. 
   
- HTTPS won’t hide critical information such as the hostname. Theoretically, an adversary can’t see the specific pages a targeted user is visiting 
   
- The purpose of HTTPS is to secure the transit but data can be intercepted in various places, for example, on web servers or databases. The data will become static eventually, so HTTPS does not make it “unhackable.” 
   
- The “s” in “HTTPS” does mean “secure” but it’s misleading, as even phishing websites can have it. 
   
