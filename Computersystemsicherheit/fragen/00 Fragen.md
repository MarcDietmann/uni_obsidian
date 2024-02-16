## [[01 Grundlagen]]
- Was sind Schutzziele
- Was sind Sicherheitsprinzipien
- Safety vs. Security
## [[02 Kryptographie]]
- Wie funktioniert CBC, ECB, CTR?
- Wie funktioniert ein OTP
- Was ist der Unterschied/ Vorteile zwischen symmetrischer und asymmetrischer Verschlüsselung?
- Wie funktioniert eine symmetrische/ asymmetrische Verschlüsselung? (Grundlegend)
- Wie funktioniert die RSA Schlüsselgeneration und Verschlüsselung damit?
- Wie funktioniert der Diffie-Hellman Schlüsselaustausch?
- Was versteht man unter hybrider Verschlüsselung?
- Wie funktionieren Signaturen?
- Was sind die Schutzziele der Kryptographie
- Welche Angriffsspiele gibt es bei der Kryptographie?
- Wie funktioniert der (erweiterte) Euklid? Wozu dient er?
- Wozu dienen Zertifikate?
## [[03 Netzwerksicherheit]]
- Wie ist das OSI Schichtenmodell aufgebaut?
- Wie ist das TCP/IP Modell aufgebaut?
- Auf was könnte es ein Angreifer bei einer Website abgesehen haben
- Was ist MAC Flooding
- Wie funktioniert ARP? Was ist ARP Spoofing?
- Wie funktioniert DHCP? Was ist DHCP Spoofing?
- Wie kann man die einzelnen Schichten im TCP/IP Modell angreifen?
- Was ist Border Gateway Controll? Was ist BGC Hijacking?
- Wie funktioniert TCP ?
- Wie funktioniert UDP
- Wie funktioniert der TLS Handshake
## [[04 Websicherheit]]
- Was ist das Web?
- Wie ist eine Url aufgebaut?
- Was ist die Same Origin Policy? 
	- Welche Urls sind alle erlaubt? (www.example.org)
- Wozu dienen Cookies?
- Was sind die häufigsten Sicherheitslücken?
- Wie kann man sich gegen SQL Injections schützten?
- Wie kann man sich gegen XSS schützen?
- Wie funktioniert CSRF?
## [[05 Systemsicherheit]]
- Welche Arten von Maleware gibt es?
- Wie kann man sich gegen einen Virus schützen? Wie umgehen Virenhersteller das?
- Was ist ein Buffer Overflow Attack? Wie kann man sich dagegen schützten?
- Welche Hardwareangriffe gibt es?

## [[06 Verknüpfende Fragen]]
- Wie sieht eine Gewinnstrategie bei einem MitM-Attack aus wenn ein OTP mehrfach benutzt wird. 
- Betrachte einen Brute Force Angriff wo der Angreifer alle Schlüssel ausprobiert, um das Verschlüsselungsverfahren anzugreifen. Bricht dieser Angreifer die IND-CPA Sicherheitseigenschaft?
- Können im CBC-Modus oder CTR-Modus Blöcke parallel verschlüsselt werden?
- Ist das Textbuch RSA Verfahren IND-CPA sicher?
- Ist das RSA Signaturverfahren ohne Hash und Encoding, also 𝑠 = 𝑚* 𝑚𝑜𝑑 𝑁, sicher?