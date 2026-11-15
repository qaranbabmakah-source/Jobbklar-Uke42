# Analyse og utvikling av IT-løsninger – Fra teori til praksis

DEL-1. IT-SYSTEMER, SYSTEMARKITEKTUR, NETTVERK OG SIKKERHET

Oppgave 1 – Analyser et IT-system
1. Hvilket IT-system har jeg valgt?

Jeg har valgt en digital læringsplattform som elevene og lærerne bruker på skolen.

2.Minst seks komponenter i systemet

a)Nettleser: Elevene bruker nettleseren for å åpne læringsplattformen.

b) Webserver: Webserveren mottar forespørsler fra nettleseren og sender nettsiden tilbake.

c)Applikasjonsserver: Den behandler informasjon og utfører oppgaver i læringsplattformen.

d) Database: Databasen lagrer informasjon om elever, lærere, fag, oppgaver og karakterer.

e) Innloggingstjeneste: Den kontrollerer brukernavn og passord når elever og lærere logger inn.

f) Nettverk: Nettverket kobler sammen datamaskinen og serverne slik at de kan kommunisere.

3. Hvilke komponenter er avhengige av hverandre?

Komponentene jobber sammen for at læringsplattformen skal fungere. Nettleseren sender forespørsler til webserveren. Webserveren sender dem videre til applikasjonsserveren. Applikasjonsserveren bruker databasen til å hente og lagre informasjon. Innloggingstjenesten sjekker hvem som kan logge inn. Nettverket gjør at alle komponentene kan kommunisere med hverandre.

                      4. Arkitekturdiagram  Digital læringsplattform

<img width="610" height="367" alt="Untitled Diagram-Page-2 drawio (2)" src="https://github.com/user-attachments/assets/3c9405bb-d3b1-4d33-9f64-07f5fea878d1" />

Jeg har laget et enkelt arkitekturdiagram som viser hvordan komponentene henger sammen. Diagrammet viser hvordan brukeren åpner læringsplattformen, og hvordan informasjon sendes mellom de forskjellige komponentene.
Rekkefølge i diagrammet
Bruker → Nettleser → Webserver → Applikasjonsserver → Database
Innloggingstjenesten kontrollerer brukeren når han eller hun logger inn. Nettverket kobler sammen komponentene


5. Hva kan skje dersom én komponent slutter å fungere?

Nettleser: Brukeren kan ikke åpne læringsplattformen i nettleseren.
Webserver: Nettsiden kan bli utilgjengelig for elevene
Applikasjonsserver: Funksjoner som å levere oppgaver kan slutte å fungere.
Database: Elevene kan få problemer med å hente oppgaver og karakterer.
Innloggingstjeneste: Elevene og lærerne kan ikke logge inn hvis tjenesten slutter å fungere.
Nettverk: Komponentene kan ikke kommunisere med hverandre hvis nettverket slutter å fungere.

Konklusjon
En digital læringsplattform består av flere komponenter som samarbeider. Alle komponentene har viktige oppgaver. Hvis én komponent slutter å fungere, kan deler av plattformen eller hele systemet slutte å fungere.


Klient–server-arkitektur og nettverk

Elevoppgave 2

Hva skjer når en nettside åpnes?
Hva er klienten?

Klienten er nettleseren eleven bruker på PC-en eller mobilen.

Hvilken oppgave har DNS?

DNS finner IP-adressen som hører til domenenavnet. Da vet nettleseren hvilken server den skal kontakte.

Hva er forskjellen mellom en IP-adresse og et domenenavn?
En IP-adresse er en talladresse, for eksempel 192.0.2.1. Et domenenavn er et navn, for eksempel skole.no. Navnet er lettere å huske. 

Hvilken funksjon har HTTPS?

HTTPS krypterer informasjonen mellom nettleseren og serveren. Det beskytter blant annet passord mot at andre leser dem under overføringen.

5. Hvorfor må serveren sende et svar tilbake?

Nettleseren trenger svaret for å vise nettsiden. Serveren sender innholdet, eller en feilmelding hvis noe er galt.
Hvorfor åpnes ikke nettsiden?
Det kan være flere grunner:

a)Eleven har ikke internett.

B)Nettadressen er skrevet feil.

C)DNS-tjenesten har problemer.

D)Serveren er nede eller har for mange brukere.

E)Nettverket blokkerer nettsiden.

Elevoppgave 3: Arkitekturen til et elevregister

1. De tre lagene

<img width="192" height="402" alt="Untitled Diagram-Page-3 drawio (2)" src="https://github.com/user-attachments/assets/0dbcfc33-475e-4fe4-bf05-8a38269d703e" />

a)Presentasjonslaget: Brukergrensesnittet som læreren ser i nettleseren.

b)Applikasjonslaget: Logikken som sjekker og behandler opplysningene.

c)Datalaget: Databasen som lagrer elever, fag og karakterer.

Hvordan registrerer læreren en karakter?

Læreren logger inn, velger elev og fag og skriver inn karakteren. Når læreren trykker «Lagre», sendes informasjonen til applikasjonslaget. Der sjekker systemet at karakteren er gyldig, og at læreren har lov til å registrere den. Deretter lagres karakteren i databasen, og læreren får en bekreftelse. 

Hvilken funksjon har et API?

Et API lar brukergrensesnittet kommunisere med applikasjonslaget. Det kan for eksempel brukes til å hente en elevliste eller sende inn en karakter.

Hvorfor skille applikasjonslogikken fra databasen?

Det gjør systemet lettere å endre og vedlikeholde. Reglene for registrering av karakterer ligger i applikasjonslaget, mens databasen lagrer opplysningene. Da kan man endre reglene uten å måtte endre selve databasen.

Hvorfor bør ikke nettleseren ha fri tilgang til databasen?

Fri tilgang kan gjøre det mulig å lese, endre eller slette opplysninger uten lov. Elever og karakterer må beskyttes. Derfor bør forespørsler gå gjennom applikasjonslaget, som kontrollerer hvem brukeren er, hva brukeren har lov til å gjøre, og om opplysningene er gyldige.




DEL-2 SYSTEMARKITEKTUR FOR ET KOMMUNALT TIMEBESTILLINGSSYSTEM



Foreslå en egnet systemarkitektur.

Jeg foreslår et digitalt system med seks komponenter: innbygger, webserver, applikasjonsserver, database, innloggingstjeneste og varslingstjeneste.

Innbyggeren bruker en mobil eller PC for å bestille time. Webserveren mottar forespørselen, og applikasjonsserveren behandler bestillingen. Databasen lagrer informasjon om timer og brukere. Innloggingstjenesten kontrollerer hvem brukeren er, og varslingstjenesten sender bekreftelser på SMS eller e-post. 

 Arkitekturdiagram.

<img width="466" height="514" alt="Untitled Diagram-Page-1 drawio" src="https://github.com/user-attachments/assets/f40f1dd2-4ded-44a6-906f-6b06c2b0bea1" />


Jeg har laget et arkitekturdiagram som viser de viktigste komponentene i systemet og hvordan de kommuniserer med hverandre.
Diagrammet har seks komponenter og viser hvordan en innbygger kan bestille, endre eller avbestille en time.

Diagrammet viser seks deler:

Innbygger: Bruker mobil eller PC til å bestille og endre timer.

Webserver: Viser nettsiden og sender forespørsler videre.

Applikasjonsserver: Behandler bestillinger og sjekker ledige timer.

Database: Lagrer bestillinger og nødvendige personopplysninger.

Innloggingstjeneste: Kontrollerer hvem brukeren er.

Varslingstjeneste: Sender bekreftelser på SMS eller e-post.

Dataflyt ved en bestilling.

Først åpner innbyggeren nettsiden og logger inn. Systemet henter ledige timer fra databasen. Innbyggeren velger en time og trykker på «Bestill».
Applikasjonsserveren sjekker at timen fortsatt er ledig og lagrer bestillingen. Kontrollen og lagringen må hindre at to personer får samme time. Innbyggeren får bekreftelse på nettsiden og på SMS eller e-post.

Ved endring eller avbestilling kontrollerer systemet at bestillingen tilhører brukeren. Databasen oppdateres, og en ny bekreftelse sendes.

Nettverksprotokoller og grensesnitt.

HTTPS beskytter informasjonen mellom nettleseren og webserveren ved å kryptere trafikken.

HTTPS kan brukes mellom webserveren og applikasjonsserveren. Et API lar delene utveksle informasjon, for eksempel ledige timer.

Lokal drift og skybasert drift.

Ved lokal drift har kommunen egne servere. Kommunen får stor kontroll, men må selv sørge for utstyr, vedlikehold, sikkerhet og nok kapasitet.
Ved skybasert drift kjører systemet hos en leverandør. Det er enklere å øke kapasiteten når mange bruker tjenesten. Samtidig blir kommunen avhengig av internett og leverandøren, og kostnadene kan øke med bruken.















