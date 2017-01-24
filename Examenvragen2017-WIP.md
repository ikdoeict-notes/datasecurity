# Examenvragen - Data Security 2017 (WIP)
###### Door Seppe Snoeck volgens samenvatting/cursus Anthony Mestdagh

1. Geef de 3 componenten van de data service en bespreek.
2. Welke acties kan je onder nemen voor stategie en beveiliging? 
3. Wat is het verschil tussen vulnerability en exploit?
4. In welke twee groepen worden hacker onderverdeeld?
5. Wat is ARP Poison routing?
6. Hoe worden interne aanvallen veroorzaakt?
7. Wat is de meest gangbare definitie van hacking?
8. Bespreek enkele policies.
9. Welke Internationate security management frameworks bestaan er?
10. Waarvoor staat ISO en wat is het verschil tussen ISO27001 en ISO27002? 
11. Wat is de inhoud van ISO27001? (BOB PerFyCT SCooR)
12. Waarvoor staat PCI-DSS en wat houd dit in? 
13. Aanvallen kunnen op elke laag van het osi model gebeuren. Geef de lagen met bijhorende aanvallen.
14. Wat is het doel van encryptie? 
15. Wanneer wordt een coderig veilig beschouwd?
16. Verklaar side channel attacks.
17. Wat is een goed algoritme voor encryptie?
18. Welke codeertechniek gebruik je voor ontvanger en zender eenzelfde sleutel en voor welke een andere?
19. Wat is het verschil tissen block en stream cypher?
20. Hoe werkt Electronic Codebook en is dit veilig?
21. Hoe werkt Cipher block Chaining?

## Antwoorden
1. **Geef de 3 componenten van de data service en bespreek.**
   
   **Confidentiality** beperkt de toegang enkel tot geautoriseerde gebruikers. Data is verkrijgbaar in drie verschillende toestanden. In transit (verzonden), At rest (opgeslagen) en In use (wordt verwerkt). Bescherming komt neer op de implementatie van ecryptie, key management en een goed authenticatie systeem. Kenmerken: tijdigheid, continuïteit en robuustheid.

   **Integrity** houd in dat data enkel mag aangepast worden door geautoriseerde gebruikers. Denk lees- en schrijfrechten op de 3 toestanden van data. Verzonden data mag onderweg niet aangepast worden door onbetrouwbare applicaties en apparaten die jezelf niet beheerd. Kenmerken: juistheid, volledigheid en geautoriseedheid.

   **Availability**  houd in dat je data steeds beschickbaar wilt houden. De gevaren van data bewaren kunnen fysiek of op het netwerk zijn. Men kan specifieke maatregelen treffen tegen aanvallen maar ook vorgen voor redundatie en backups.

2. **Welke acties kan je onder nemen voor stategie en beveiliging?**

   Preventive (firewall), corrective (update) & detective (ips, virusscan) actions
   
3. **Wat is het verschil tussen vulnerability en exploit?**
   
   **Vulnerability** is een kwetsbaarheid. Deze krijgen telkens een uniek nummer mee voor identificatie. CVE-\<jaar\>-xxxx
   
   Een **Exploit** toont aan hoe een vulnerability kan misbruikt worden.
   
4. **In welke twee groepen worden hacker onderverdeeld?**

   **Extene aanvallers** zijn altijd strafbaar. **Interne** aanvallers zijn enkel strafbaar wanneer men schade wil toebrengen.

5. **Wat is ARP Poison routing?**

   Een techniek waarbij een aanvaller een spoofed Adress Resolution Protocol (ARP) berichten verzend in een locaal netwerk. De bedoeling is om het MAC-address van de aanvaller te linken met een ip-address van een andere host, bv de default gateway. Het gevolg hiervan is dat het verkeer bestemt voor dat adress ook toekomt bij de aanvaller. Men kan verkeer onderscheppen, aanpassen of volledig stop zetten. Deze techniek word meestal gebruikt om na dien verder te hacken naar een dos, mitm of sessions hacking. Dit kan natuurlijk alleen gebruikt worden bij netwerken die ARp-protocal gebruiken en is gelimiteerd tot 'local network segments'.
   
6. **Hoe worden interne aanvallen veroorzaakt?**

   Door **legitime gebruikers** met kwaad opzet of om goede bedoeling die misbruikt worden. bv Een slechte wifi dekking oplossen et een eigen acces point. **Mobiele apparaten** door diefstal of gebruik buiten een gecontroleerde omgeving. **Leveranciers** (PoS Attack: HVAC company) 
   
   !! Kan iemand leveranciers nog verduidelijken? !!
   
7. **Wat is de meest gangbare definitie van hacking?**
   
   Het ongeoorloofd binnendringen in een computersysteem.
   
8. **Bespreek enkele policies**

   **Information security policy**: Beschrijft waarvoor en hoe IT-systemen gebruikt worden.
   
   **Information protection policy**: Beschrijft wie toegang geeft tot informatie, hoe die verspreid mag worden en het gevoeligheidsniveau. 
   
   **Password policy**: Beschrijft hoe wachtwoorden moeten opgebouwd worden.
   
   **Email policy**: Beschrijft Hoe, wanneer en wat geaudit moet worden door wie.
   
9. **Welke Internationale security management frameworks bestaan er?**

  ISO27001 & ISO 27002
  
  PCI-DSS
  
  Common Criteria
10. **Waarvoor staat ISO en wat is het verschil tussen ISO27001 en ISO27002?**
  International Standard Organisation. **ISO27001** Bevast standaard richtlijnen om zelf policies te ontwikkelen en kan op elk bedrijf toegepast worden.**ISO27002** bevat praktische richtlijnen over hoe iso27001 kan geï 
  PCI-DSSmplementeerd worden.
  
11. **Wat is de inhoud van ISO27001?**
  * Beleidsmatig
  * Organisatorisch
  * Bedrijfsmiddelen
  * Personeel
  * Fysiek
  * Communicatie en operatie
  * Toegangscontrole
  * Systeem-en softwareontwikkeling en onderhoud
  * Continuïteit
  * Regelgeving

12. **Waarvoor staat PCI-DSS en wat houd dit in?**

  Payment Card Industry - Data Security Standard is een 'checklist' van praktische regels waar aan een bedrijf moet voldoen dat krediet kaart informatie gebruikt. Indien je niet voldoet kan je aansprakelijk gesteld worden vaar de schade.
  
13. **Aanvallen kunnen op elke laag van het osi model gebeuren. Geef de lagen met bijhorende aanvallen.**

  * L8: Humans
    * Social engeneering, phishing, malifide mails
  * L7: Aplication
    * CSS, SQLi, gevoelige info via foutmeldingen
  * L6: Presentation
    * Http attacks, SSL tunneling
  * L5: Session
    * Exploits op Telnet
  * L4: Transport
  * L3: Network
  * L2: Data link
    * Network trafic sniffing, Arp spoofing / poisoning
  * L1: Physical
    * Diefstal, ongeautoriseerde toegang tot computer of lokaal, aangepaster firmwares

14. **Wat is het doel van encryptie?**
  Data coderen naar een onherkenbaar formaat. Gemakkelijk omkeerbaar voor doelpublie maar moeilijk voor onbekenden. Bewaken van intergiteit.
  
15. **Wanneer wordt een coderig veilig beschouwd?**
   
   Een codering kan veilig beschouwd worden als de waarde van de beschermde gegevens lager ligt dan de kost van de aanval. 

16. **Verklaar side channel attacks.**
   
   Side channel attacks vallen de codering niet rechtstreeks aan. bv iPhone keylogger.
   
17. **Wat is een goed algoritme voor encryptie?**

    Een goed algoritme beschermt date op basis van een (geheime) sleutel. Het algoritme is publiekelijk beschikbaar en gebruikt bestaande algoritmes. 
    
18. **Welke codeertechniek gebruik je voor ontvanger en zender eenzelfde sleutel en voor welke een andere?**
   **symmetrische codering** -> Eenzelfde sleutel die geheim is. -> **Secret key**
   
   **assymmetrische codering** -> Beide partijen gebruiken verschillende sleutels waarvan éé van beide publiek kan gemaakt worden naargelang jouw toepassing -> **Public Key**
   
   Zender aka encryptie, ontvanger aka decryptie
   
 19. **Wat is het verschil tissen block en stream cypher?**
   
   Bij ** block cypher** wodt de data verdeeld in blokken van een bepaalde grootte. Wanneer een datastroom versleuteld worden betekend dat dat de stroom onderverdeeld moet worden in een aantal blokken. De stroom zal eventueel vergroot worden door paddingbits om blokken van gelijke groote te bekomen.
   
   Bij **stream cypher** wordt de datastroom symbool per symbool versleuteld. Dit gaat sneller maar is beperkt in zijn hoeveelheid gegevens en kan minder complexere operaties uitvoeren.
   
20. **Hoe werkt Electronic Codebook en is dit veilig?**
   ECB is een methode waarbij men data splitst in blokken. Het encryptiealgoritme zal dan een aantal keer herhaald worden op de opeenvolgende blokken met hetzelfde ecnryptiealgoritme en sleutel voor elke blok. Het nadeel is dat deze methode veel informatie prijs geeft. Dit verlaagd de confidentiality en is zeker niet veilig/aangewezen voor gebruik.
   
21. **Hoe werkt Cipher block Chaining?**
   Bij CBC gebruik je de cipher tekst van het vorige blok om het volgende tekst blok te vervormen alvorens je encypteert. De ontvanger beschikt over het nodige ciperblok m na decryptie het resultaat terug te kunnne vormen naar de juiste plain tekst. Echter moet er afgesproken worden welke initail vector (IV) er gebruikt wordt bij het eerste blok.
