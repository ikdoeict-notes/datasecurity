# Examenvragen - Data Security 2017 (WIP)
###### Door [Seppe Snoeck](https://www.github.com/AllUsernamesHaveBeenTaken) volgens [samenvatting/cursus](https://www.github.com/ikdoeict-notes/datasecurity/blob/master/samenvatting-AnthonyMestdach/DataSecurity.docx) Anthony Mestdagh

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
19. Wat is het verschil tussen block en stream cypher?
20. Hoe werkt Electronic Codebook en is dit veilig?
21. Hoe werkt Cipher block Chaining?
22. Hoe voldoe je aan alle eisen voor asymmetrische encripty?
23. Wat is MAC?
24. Wat is het verschill tussen https, ssl en tsl?
25. Wat is HSTS?
26. Wat is SPF?
27. Hoe kan je een paswoord achterhalen en wat kan je doen al tegenmaatregel?
28. Aan welke eisen moet een user en autenticator voeldoen voor een veilig(e omgang met) paswoord?
29. Hoe sla je paswoorden het best op in bv. een databank?
30. Wat is de functie van salt?
31. Leg de werking uit van biometrische authenticatie. Twee methoden.
32. Wat is het verschil tussen IDS en IPS?
33. Geef drie dedectie systemen binnen NIPS.
34. Wat is een Honneypot?
35. Verduidelijk virus, worm, rootkit en trojan.

## Antwoorden
1. **Geef de 3 componenten van de data service en bespreek.**
   
   **Confidentiality** beperkt de toegang enkel tot geautoriseerde gebruikers. Data is verkrijgbaar in drie verschillende toestanden. In transit (verzonden), At rest (opgeslagen) en In use (wordt verwerkt). Bescherming komt neer op de implementatie van encryptie, key management en een goed authenticatie systeem. Kenmerken: tijdigheid, continuïteit en robuustheid.

   **Integrity** houd in dat data enkel mag aangepast worden door geautoriseerde gebruikers. Denk lees- en schrijfrechten op de 3 toestanden van data. Verzonden data mag onderweg niet aangepast worden door onbetrouwbare applicaties en apparaten die jezelf niet beheerd. Kenmerken: juistheid, volledigheid en geautoriseerdheid.

   **Availability**  houd in dat je data steeds beschikbaar wilt houden. De gevaren van data bewaren kunnen fysiek of op het netwerk zijn. Men kan specifieke maatregelen treffen tegen aanvallen maar ook zorgen voor redundantie en backups.

2. **Welke acties kan je onder nemen voor stategie en beveiliging?**

   Preventive (firewall), corrective (update) & detective (ips, virusscan) actions
   
3. **Wat is het verschil tussen vulnerability en exploit?**
   
   **Vulnerability** is een kwetsbaarheid. Deze krijgen telkens een uniek nummer mee voor identificatie. CVE-\<jaar\>-xxxx
   
   Een **Exploit** toont aan hoe een vulnerability kan misbruikt worden.
   
4. **In welke twee groepen worden hacker onderverdeeld?**

   **Externe aanvallers** zijn altijd strafbaar. **Interne** aanvallers zijn enkel strafbaar wanneer men schade wil toebrengen.

5. **Wat is ARP Poison routing?**

   Een techniek waarbij een aanvaller een spoofed Adress Resolution Protocol (ARP) berichten verzend in een lokaal netwerk. De bedoeling is om het MAC-adres van de aanvaller te linken met een ip-adres van een andere host, bv de default gateway. Het gevolg hiervan is dat het verkeer bestemt voor dat adres ook toekomt bij de aanvaller. Men kan verkeer onderscheppen, aanpassen of volledig stop zetten. Deze techniek word meestal gebruikt om na dien verder te hacken naar een dos, MITM of sessions hacking. Dit kan natuurlijk alleen gebruikt worden bij netwerken die ARP-protocol gebruiken en is gelimiteerd tot 'local network segments'.
   
6. **Hoe worden interne aanvallen veroorzaakt?**

   Door **legitime gebruikers** met kwaad opzet of om goede bedoeling die misbruikt worden. bv Een slechte wifi dekking oplossen et een eigen acces point. **Mobiele apparaten** door diefstal of gebruik buiten een gecontroleerde omgeving. **Leveranciers** (PoS Attack: HVAC company) 
   
   !! Kan iemand leveranciers nog verduidelijken? !!
   
7. **Wat is de meest gangbare definitie van hacking?**
   
   Het ongeoorloofd binnendringen in een computersysteem.
   
8. **Bespreek enkele policies**

   **Information security policy**: Beschrijft waarvoor en hoe IT-systemen gebruikt worden.
   
   **Information protection policy**: Beschrijft wie toegang geeft tot informatie, hoe die verspreid mag worden en het gevoeligheidsniveau. 
   
   **Password policy**: Beschrijft hoe wachtwoorden moeten opgebouwd worden.
   
   **Email policy**: Beschrijft Hoe, wanneer en wat geauditeerd moet worden door wie.
   
9. **Welke Internationale security management frameworks bestaan er?**

  ISO27001 & ISO 27002
  
  PCI-DSS
  
  Common Criteria
10. **Waarvoor staat ISO en wat is het verschil tussen ISO27001 en ISO27002?**
  International Standard Organisation. **ISO27001** bevat standaard richtlijnen om zelf policies te ontwikkelen en kan op elk bedrijf toegepast worden.**ISO27002** bevat praktische richtlijnen over hoe ISO27001 kan geïmplementeerd worden.
  
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

  Data coderen naar een onherkenbaar formaat. Gemakkelijk omkeerbaar voor doelpubliek maar moeilijk voor onbekenden. Bewaken van integriteit.
  
15. **Wanneer wordt een coderig veilig beschouwd?**
   
   Een codering kan veilig beschouwd worden als de waarde van de beschermde gegevens lager ligt dan de kost van de aanval. 

16. **Verklaar side channel attacks.**
   
   Side channel attacks vallen de codering niet rechtstreeks aan. bv iPhone keylogger.
   
17. **Wat is een goed algoritme voor encryptie?**

    Een goed algoritme beschermt date op basis van een (geheime) sleutel. Het algoritme is publiekelijk beschikbaar en gebruikt bestaande algoritmes. 
    
18. **Welke codeertechniek gebruik je voor ontvanger en zender eenzelfde sleutel en voor welke een andere?**
   **symmetrische codering** -> Eenzelfde sleutel die geheim is. -> **Secret key**
   
   **assymmetrische codering** -> Beide partijen gebruiken verschillende sleutels waarvan éé van beide publiek kan gemaakt worden naargelang jouw toepassing -> **Public Key**
   
   Zender a.k.a. encryptie, ontvanger a.k.a. decryptie
   
19. **Wat is het verschil tussen block en stream cypher?**
   
   Bij **block cypher wordt** wodt de data verdeeld in blokken van een bepaalde grootte. Wanneer een datastroom versleuteld worden betekend dat dat de stroom onderverdeeld moet worden in een aantal blokken. De stroom zal eventueel vergroot worden door padding bits om blokken van gelijke grootte te bekomen.
   
   Bij **stream cypher** wordt de datastroom symbool per symbool versleuteld. Dit gaat sneller maar is beperkt in zijn hoeveelheid gegevens en kan minder complexere operaties uitvoeren.
   
20. **Hoe werkt Electronic Codebook en is dit veilig?**

   ECB is een methode waarbij men data splitst in blokken. Het encryptiealgoritme zal dan een aantal keer herhaald worden op de opeenvolgende blokken met hetzelfde ecnryptiealgoritme en sleutel voor elke blok. Het nadeel is dat deze methode veel informatie prijs geeft. Dit verlaagd de confidentiality en is zeker niet veilig/aangewezen voor gebruik.
   
21. **Hoe werkt Cipher block Chaining?**

   Bij CBC gebruik je de cipher tekst van het vorige blok om het volgende tekst blok te vervormen alvorens je encypteert. De ontvanger beschikt over het nodige cipherblok om na decryptie het resultaat terug te kunnen vormen naar de juiste plain tekst. Echter moet er afgesproken worden welke initial vector (IV) er gebruikt wordt bij het eerste blok.

22. **Hoe voldoe je aan alle eisen voor asymmetrische encripty?**

   Door tweemaal asymmetrische encryptie toe te passen. De eerste keer met de publieke sleutel voor vertrouwlijkheid en een tweede keer met de private sleutel voor integriteit, authenticatie en non-repudiatie.

23. **Wat is MAC?**

   Message Authentication Codeis een stuk data dat aan een bericht toegevoegd wordt om te verifiëren dat de date niet aangepast werd na het versturen van bij de verzender. 

24. **Wat is het verschill tussen https, ssl en tsl?**

   Met **https** wordt aangegeven dat het verkeer over een secure kanaal gaat. **Ssl** is een protocal voor het beveiligen van http verkeer. Maar dit is verouderd. **Tsl** is de opvolger van ssl. De eerste versie bood niks meer aan dan sslv3, recentste versie is tslv1.3.

25. **Wat is HSTS?**

   Header Strict Transport Security is een manier om SSLstrip-achtige aanvallen tegen te gaan. Het forceert https-connecties voor (sub)domeinen. Dit wordt toegevoegd aan de header bij de eerste request naar de site.

26. **Wat is SPF?**

   Sender Policy Framwork is een email validatie systeem om email spoofing te detecteren. Kan aanvaard worden als anti spam techniek.

27. **Hoe kan je een paswoord achterhalen en wat kan je doen al tegenmaatregel?**

   **Sniffing**, zo probeert een aanvaller het paswoord van een gebruiker te onderscheppen bij het aanmelden over het netwerk. Een tegenmaatregel kan zijn: het niet clear text verzenden van paswoorden.

   Wanneer het **gebruikersID gekent** is kan een aanvaller het passwoord raden met de kennis over de gebruiker die aldan niet online te vinden is. Dit kan in vorm van een **online** en **offline attack**. Een online tegen maatregel kan zijn: het gebruik maken van een lockout systeem dat ernstige vertraging kan opleveren bij het gokken/aanvallen. Voor een offline attack moet de aanvaller eerst de opgeslagen paswoorden te pakken zien te krijgen, nadien kan alles ver gebeuren binnen eigen infrastucturen. Maatregelen hiertegen zijn: Het niet cleartext opslaan van passwoorden en zorgen dat deze files nooit gestolen kunnen worden. 

28. **Aan welke eisen moet een user en autenticator voeldoen voor een veilig(e omgang met) paswoord?**
   
   **User**: 
    * Lengte
    * Karakters
    * Hoe onthouden

   **Authenticator**:
    * oplag paswoord
    * transmissie van authenticatiegegevens
    * contolr van authenticatiegegevens

29. **Hoe sla je paswoorden het best op in bv. een databank?**
  
  NIET ALS CLEAR TEXT!

  Jen kan je volledige databank encypteren maar dat is geen goed idee want dan worden alle paswoorden versleuteld met dezelfde sleutel. Je berekent best voor elk paswoord een hash en je slaat die hash op. Wanneer één paswoord is achterhaald blijven de andere geheim. Bij het controleren/inloggen wordt het ingegeven paswoord ook gehashed en worden de hashes met elkaar vergeleken want een hash in onomkeerbaar. Een aanvaller zal ook op eenzelfde manier te werk moeten gaan.

30. **Wat is de functie van salt?**

   Salt is een techniek om voor gelijke paswoorden een verschillend hash te berekenen. Zo wordt een random patroon toegevoegd aan het paswoord alvorens de hash berekend wordt. De gebruikte salt wordt opgeslaan zoadat bij contole deze kan toegevoegd worden bij het ingegeven paswoord.

   Wanneer nu een aanvaller een veel voorkomen paswoord wilt testen met de hashes in een databank moet hij ook alles salts van de databank toevoegen aan het paswoord. Wat dan weer vertraging oploopt voor de aanvaller.

   Ook voor de gebruiker zal dit vertraging oplopen bij het inloggen maar dit is miniem zeker in vergelijking met een aanval op een databank. 

31. **Leg de werking uit van biometrische authenticatie. Twee methoden.**

   **Verificatie**: De gebruiker geeft informatie over zijn identiteit en wordt die geverifiërd aan de hand van de biometrische gegevens.

   **Identificatie**: Er wordt in alle user templates gezocht naar een match. De gebruiker krijgt de identiteit van de user template waarmee een match is gevonden.

32. **Wat is het verschil tussen IDS en IPS?**

   **Intrusion Detection System** dedecteerd problemen en rapporteert ze. Vaak offline, wordt aan een SPAN-poort gekoppelt om een kopie van het verkeer te inspecteren. --> volledig onzichtbaar voor een aanvaller.

   **Intrusion Prevention System** kan zelf ingrijpen op het netwerkverkeer (vb. connecties sluiten). Het verkeer moet door dit toestel. 

33. **Geef drie dedectie systemen binnen NIPS.**
   
   Signature, Anomalie en Protocal anomalie detectie.

34. **Wat is een Honneypot?**

   Een IT-systeem dat is opgezet om aanvallers te lokken die het netwerk aanvallen.

35. **Verduidelijk virus, worm, rootkit en trojan.**

   Een **virus** is malware dat moet uitgevoerd worden. Het infecteerd andere bestanden komt voor als poly-(veranderd bij elke infectie) en metamorf(herschrijft zichzelf).

   Een **worm** verspreid zichzelf door actief te zoeken naar slachtoffers.

   **Rootkit** is een malware die zich in het OS nestelt en is erg moeilijk detecteerbaar.

   Een **trojan** is malware dat zich anders voordoet.
