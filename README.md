# Certificate Pinning in Xamarin

######First a little story..

You were at work someday, and the delivery man brings in a package with your name on it. You open it up and find therein an all too familiar invitation card to an exclusive party. The kind of party you are not too proud to tell your partner about. It made you feel special and you decide to honour it again. Afterall it's been a while since the last time, and these guys who simply go by the name; **the organisers** are really discrete and you have only had emense fun all the previous times. 

You get to the venue on the said day, present your pass at the entrance and you are granted access into the building. Only for you to get inside to discover that the party was all a set up. Apparently, you have been cajouled by the most dreaded criminal syndicate in town:  **the men in the middle**. These guys are known to have taken people against there will, forced out vital information from them, which they will go on to use to defraud their victims with. is a  you are held against your will and vital information about your credit card and bank accounts was taken off of you. You would later discover that you have been robbed clean of all your money.

You did not expect that a bunch of criminals will pose as the organisers of a private event that you attend. But if you had a way to verify from your end that the invitation was authentic and from a trusted source. You would have known that it was all a setup and thus prevented the mishap.

######Technically speaking..
**Certificate Pinning** is a security practice and or ideology that ensures end-to-end security between clients and host systems through pinning the public key. A system that implements certificate pinning will no longer be dependent on other sources such as DNS and CA for ensuring trust. Hence, will now be secured against man-in-the-middle attacks and data sniffing.

According to www.owasp.org:
>  An application which pins a certificate or public key no longer needs to depend on others - such as DNS or CAs - when making security decisions relating to a peer's identity.

In practice, pinning means to associate the [X509 public key](https://en.wikipedia.org/wiki/X.509) of the host to with the client application. In such a way that whenever a call to the host is to be made the client compares the live host's public key to a hardcoded(or a set of allowed hosts) public key in the client application. If both matches, then a secure communication line has been.

Read more about certificate pinning at [www.owasp.org](https://www.owasp.org/index.php/Certificate_and_Public_Key_Pinning)

## Implementation in Xamarin 
