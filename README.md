# Certificate Pinning in Xamarin
In simple words, **Certificate Pinning** is a security practice and or ideology that ensures end-to-end security between clients and host systems. A system that implements certificate pinning will no longer be dependent on other sources such as DNS and CA for ensuring trust. Hence, will now be secured against man-in-the-middle attacks and data sniffing.

According to www.owasp.org:
>  An application which pins a certificate or public key no longer needs to depend on others - such as DNS or CAs - when making security decisions relating to a peer's identity.

In practice, pinning means to associate the [X509 public key](https://en.wikipedia.org/wiki/X.509) of the host to with the client application. In such a way that whenever a call to the host is to be made the client compares the live host's public key to a hardcoded(or a set of allowed hosts) public key in the client application. If both matches, then a secure communication line has been.

Read more about certificate pinning at [www.owasp.org](https://www.owasp.org/index.php/Certificate_and_Public_Key_Pinning)
