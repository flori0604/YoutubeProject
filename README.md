# YoutubeProject










CLOUD COMPUTING

Crearea unei aplicatii web/mobile care sa utilizeze doua servicii in Cloud, prin intermediul unui API REST
 
Table of Contents
1. Introducere	3
2. Descrierea serviciilor folosite	3
Google Cloud Platform	3
Microsoft Azure	3
3. Descriere API	4
YouTube Data API v3	5
4.Arhitectura aplicatiei	5
5. Stocarea aplicatiei web in Microsoft Azure	10
6.Demonstrarea aplicatiei	16
BIBLIOGRAFIE	17


























1.	Introducere

În cadrul acestui proiect, am aratat cum functioneaza serviciile in cloud si cum sunt folosite in aplicatie. Am folosit un cunoscut API oferit de Google din lista celor disponibile: GoogleMaps, Gmail, Youtube, Calendar, Weather și lista poate continua. 
Totodata, arhitectura aplicatiei a fost prezentata, modul in care a fost implementata aplicatia si limbajele de programare folosite: HTML, CSS si Javascript.

2. Descrierea serviciilor folosite

Google Cloud Platform

In proiectul prezent am folosit un-API de la Google, Youtube Data v3. API-urile Google Cloud sunt interfețe programatice pentru serviciile Google Cloud Platform. Acestea sunt o parte esențială a Platformei Google Cloud, permițându-vă să adăugați cu ușurință puterea tuturor lucrurilor, de la calcul la rețea la stocare, până la analiza datelor bazată pe învățarea automată în aplicațiile dvs.
     API-urile din cloud sunt expuse ca servicii API de rețea clienților, cum ar fi Cloud Pub/Sub API. Fiecare API Cloud rulează de obicei pe una sau mai multe subdomenii și oferă atât interfețe JSON HTTP, cât și gRPC clienților prin internet public și rețele Virtual Private Cloud (VPC). Clienții pot trimite solicitări HTTP și gRPC către punctele finale cloud API direct sau utilizând bibliotecile client.googleapis.compubsub.googleapis.com.
Pentru a vedea API-urile Cloud disponibile, consultați API-urile Google Cloud în Biblioteca API a consolei Google Cloud.

Pentru stocarea aplicatiei web, am folosit serviciile de cloud computing operate de Microsoft, si anume Microsoft Azure.


Microsoft Azure

Azure a fost creat în 2010 de Microsoft pentru a furniza servicii cloud în care utilizatorii își puteau construi, testa, implementa și gestiona aplicațiile în centrele de date ale Microsoft. Aceste centre de date au fost răspândite în 54 de regiuni globale. Microsoft oferă diverse servicii în mai multe domenii, cum ar fi Compute, Database, Content Delivery, Networking și multe altele.

Exista o multitudine de servicii oferite de Azure, care pot fi clasificate dupa cum urmeaza:
1.	Azure Compute
2.	Azure Networking
3.	Azure Storage
4.	Baza de date Azure


Azure Compute
Prin serviciul de compute, se ofera produse care determina executarea unei aplicatii implementate in platforma Azure, precum:
-	Azure Virtual Machine
-	Azure Container Service
-	Azure Batch
-	Azure Cloud Services
-	Azure Web Apps
-	Azure Event Hub

Azure Networking
Aceste retele permit conectarea in siguranta la resursele din cloud prin Azure ExpressRoute. De asemenea, este utilizat pentru a gestiona retelele virtuale private si, in continuare, pentru a crea mai multe retele virtuale.
-	Azure Virtual Network
-	Azure Load Balancer
-	Azure Traffic Manager
-	Azure DNS
-	Azure VPN Gateway

Azure Storage
Stocarea in Azure ofera servicii durabile cu care se pot construe aplicatii la scara larga. Totodata, este posibila echilibrarea automata a datelor in functie de traffic.
-	Azure Blob Storage
-	Azure File Storage
-	Azure Table Storage

Azure Database
Baza de date Azure este o baza de date relationala, fiabila si sigura, care ofera performante ridicate fara a fi nevoie de mentenanta la nivel de infrastructura.
-	Baza de date SQL Azure
-	Azure DocumentDB
-	Azure Redis Cache

3. Descriere API

Application Programming Interface (API) reprezintă un set de definiții de sub-programe, protocoale si unelte pentru programarea de aplicații si software. Un API poate fi pentru un sistem web, sistem de operare, sistem de baze de date, hardware sau biblioteci software. De exemplu, când este vorba despre interfața dintre programele de aplicație și sistemul de operare, acesta stabilește în amănunt modul în care programele de aplicație pot accesa (apela) serviciile sistemului de operare sub care ruleaza.

       
YouTube Data API v3

          Interfața de programare a aplicațiilor YouTube sau API-ul YouTube permite dezvoltatorilor să acceseze statisticile video și canalele YouTube prin intermediul a două tipuri de apeluri, REST și XML-RPC. Google descrie resursele API YouTube ca "API-uri și instrumente care vă permit să aduceți experiența YouTube pe pagina web, pe aplicație sau pe dispozitiv". 
Acest API se poate dezvolta in limbajele de programare enumerate mai jos:
•	Apps Script
•	Go
•	Java
•	Javascript
•	.NET
•	PHP
•	Python
•	Ruby

4.	Arhitectura aplicatiei

Obiectivul aplicatiei web este de a oferi utilizatorilor un acces mai rapid la canalul “Azure Academy”, mai exact la playlist-ul “Azure Fundamentals”.
Ca si functionalitati, pagina web va afisa primul videoclip din playlist, urmat de restul videoclipurilor, sub forma de playlist. Pe langa video, se vor afisa detalii despre fiecare videoclip incarcat, si anume: titlul, descrierea, numarul de vizualizari, durata.
Aplicatia Web foloseste, cum am mentionat la sectiunea 1, un API de la Google Cloud Platform (SaaS), si anume, Youtube Data API v3, si un serviciu de host (PaaS/IaaS) oferit de Microsoft, si anume, Microsoft Azure. Pentru dezvoltarea aplicatiei, am folosit cele mai cunoscute limbaje de programare: JavaScript, HTML, CSS
HTML este o formă de marcare orientată către prezentarea documentelor text pe o singura pagină, utilizând un software de redare specializat, numit agent utilizator HTML, cel mai bun exemplu de astfel de software fiind browserul web. HTML furnizează mijloacele prin care conținutul unui document poate fi adnotat cu diverse tipuri de metadate și indicații de redare. Indicațiile de redare pot varia de la decorațiuni minore ale textului, cum ar fi specificarea faptului că un anumit cuvânt trebuie subliniat sau că o imagine trebuie introdusă, până la scripturi sofisticate, hărți de imagini și formulare. Metadatele pot include informații despre titlul și autorul documentului, informații structurale despre cum este împărțit documentul în diferite segmente, paragrafe, liste, titluri etc. și informații cruciale care permit ca documentul să poată fi legat de alte documente pentru a forma astfel hiperlink-uri (sau web-ul).
JavaScript (JS) este un limbaj de programare orientat obiect bazat pe conceptul prototipurilor.[5] Este folosit mai ales pentru introducerea unor funcționalități în paginile web, codul JavaScript din aceste pagini fiind rulat de către browser. Limbajul este binecunoscut pentru folosirea sa în construirea siturilor web, dar este folosit și pentru accesul la obiecte încastrate (embedded objects) în alte aplicații. 
CSS (Cascading Style Sheets) este un standard pentru formatarea elementelor unui document HTML. Stilurile se pot atașa elementelor HTML prin intermediul unor fișiere externe sau în cadrul documentului, prin elementul <style>și/sau atributul style. CSS se poate utiliza și pentru formatarea elementelor XHTML, XML și SVGL.
Mai jos am prezentat pasii pe care i-am parcurs pentru dezvoltarea aplicatiei:

1.	Activarea API-ului pe platforma GCP.
Pentru a putea utiliza acest API trebuie sa urmarim pasii de mai jos:

1.1.	 Se acceseaza site-ul: https://console.cloud.google.com
 

1.2.	Se creaza un proiect nou
 
1.3.	Se introduc detaliile despre proiect

         
          


1.4.	Se activeaza YouTube Data API v3

 



1.5.	Se genereaza cheia

 

             

             


2.	Crearea unui Azure Storage

 

3.	Dezvoltarea aplicatiei in HTML, Javascript, CSS

Pentru ca aplicatia sa foloseasca API-ul oferit de Google Cloud Platform, vom folosi cheia generata anterior. Cheia se regaseste in figura de mai jos, in variabila “key”.
 

Pe langa cheia din zona de credentials, vom avea nevoie si de cheia corespunzatoare playlist-ului de pe youtube si URL-ul preluat de pe site-ul google developers.
Cum am prezentat anterior, scopul proiectului este de a afisa primul video din playlistul al caurui id este trimis ca parametru, iar celelalte videoclipuri existente in playlist, vor fi afisate intr-o lista.
Pentru a atinge acest obiectiv, am create functia de mai jos:
 
Prin acesta functie este posibila afisarea centrala, a video-ului de pe pozitia 0, urmand ca celalalte 19, sa fie afisate ca si playlist.
Pentru a afisa caracteristicile fiecarui video (imagine, titlul videoclipului, descriere,id), folosim urmatoarele variabile:

 


Pentru a aplica un stil customizat, am folosit CSS extern:
 

5. Stocarea aplicatiei web in Microsoft Azure

Azure ofera servicii de stocare, fara costuri, a website-urilor. Pentru a beneficia de acest serviciu, este nevoia indeplinirii urmatoarelor conditii:
1.	Cont Azure si subscriptie.
2.	Crearea unui Azure Storage Account.
3.	Instalarea Visual Studio Code.
4.	Extensia Azure Storage.

Dupa parcurgerea conditiilor de mai sus, am urmarit pasii urmatori:
1.	Accesarea editorului Visual Studio Code si instalarea extensiei Azure Storage
 

2.	Instalarea extensiei Azure Storage
 

Configurarea serviciului de hosting

1.	Accesarea portalului Azure (https://portal.azure.com/)
2.	Crearea unui storage account.

 

3.	Crearea unui website static

 


 

 


Deploy-ul website-ului pe Azure

1.	Crearea unui folder local.
 


2.	In Visual Studio Code, se deschide folder-ul creat local.
 


3.	Dupa ce s-a deschis folderul, se vor crea doua fisiere html (index.html si 404.html).
 

4.	Pentru a incepe deploy-ul, se va apasa click dreapta pe folderul proiectului si se va selecta “Deploy to Static Website”.

 

5.	Se selecteaza storage-ul creat in Azure.

 

6.	Dupa ce deployment-ul a fost finalizat, se poate accesa website-ul.

 








7.	Aplicatia finala

 
 
6.Demonstrarea aplicatiei

Mai multe detalii despre cum a fost construita aplicatia si se servicii au fost folosite, pot fi gasite accesand link-ul urmator: Tapu Florina cloud computing - YouTube































BIBLIOGRAFIE

https://ro.wikipedia.org/wiki/Cascading_Style_Sheets
https://ro.wikipedia.org/wiki/JavaScript
https://ro.wikipedia.org/wiki/HyperText_Markup_Language
https://console.developers.google.com
https://developers.google.com/
https://azurelessons.com/
Playlists: list  |  YouTube Data API  |  Google Developers
What is Azure—Microsoft Cloud Services | Microsoft Azure
Application Programming Interface - Wikipedia
Azure documentation | Microsoft Docs
How To Host A Website On Azure - Azure Lessons






