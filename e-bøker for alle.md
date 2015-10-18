e-bøker for alle
================

1. E-bøker for alle!
    Hei, jeg heter Jostein og kommer fra Norsk lyd- og blindeskriftbibliotek, og jeg vil fortelle litt om hvordan dere kan produsere bøker på en måte som gjør de tilgjengelige for så mange mennesker som mulig.

2. Litt kort om NLB først
  - Vi er et offentlig bibliotek som produserer og låner ut lydbøker og punktskriftbøker.
  - Tilbudet er for alle som strever med å lese trykt tekst, enten det skyldes dysleksi, synsvansker eller andre funksjonsnedsettelser som gjør det vanskelig å lese.
  - Vi har lånere fra hele landet, og tilbudet er gratis.
  - Vi produserer skjønnlitteratur og sakprosa for både barn, ungdom og voksne.
  - I tillegg så produserer vi studielitteratur for studenter ved høyere utdanning.

3. Universell utforming (TODO: trenger illustrasjon)
  - Universell utforming det betyr at *"hovedløsningen"* skal benyttes av flest mulig.
  - En universelt utformet bok er altså ikke en separat versjon tilpasset en enkelt brukergruppe, men den samme boka som alle andre bruker.

4. De fleste har på et tidspunkt også hatt en funksjonsnedsettelse
  - 17 % av Norges befolkning er registrert med en midlertidig eller varig funksjonsnedsettelse, i følge tall fra SSB. Det vil si omtrent en halv million mennesker.
  - Men dette kan være litt misvisende. Dere har eller har hatt en funksjonsnedsettelse hvis dere for eksempel:
    + har hørselsproblemer
    + er blind
    + er fargeblind
    + har dysleksi
    + bruker briller eller kontaktlinser
    + har adhd
    + har vært gravid
    + har brukket en arm eller et bein (og har gips pga det)
    + ikke har norsk som primærspråk
    + har vært full noen gang
    + har vært trøtt fordi man har vært oppe med småbarn hele natten
    + eller har hatt vondt i hodet
  - Jeg vil tro de fleste har opplevd noe av det her. Vi har alle hatt en funksjonsnedsettelse på et eller annet tidspunkt.
  - Universell utforming er altså viktig ikke bare for de som har en *"registrert"* funksjonsnedsettelse men for de aller aller fleste.

5. I tillegg så er vi alle utsatt for funskjonshemninger, eller *situasjonsbetingte lesevansker*
  - Hvis man leser på en **mobiltelefon** så har man kun tilgang til en liten porsjon tekst om gangen. Da har man den samme utfordringen som de som ser dårlig og trenger å forstørre teksten på PC-skjermen. Det er også samme utfordring som de som er blinde har når de leser punktskrift.
  - Hvis det blir for **mørkt** til å lese, så vil man kanskje sette pris på å kunne veksle mellom tekst-versjonen av boka og lydboka. Da har man den samme utfordringen som de som er tilnærmet eller helt blinde.
  - Hvis man leser ute **i sola** så vil man oppleve problemer med kontraster. Det er stor variasjon i lysforhold og skjermkvalitet der folk leser. God kontrast er viktig for folk med fargeblindhet og for de med nedsatt kontrastfølsomhet, som vanligvis følger med aldring.
  - Hvis man sitter **på toget eller bussen** og leser en nettavis så vil mange kanskje unngå å se videoer de kommer over i nyhetsartikler for å ikke forstyrre medpassasjerene. Hvis videoen hadde hatt undertekster så ville det vært greit å se videoen med lyden avslått. Dette ville også gjort videoen mer tilgjengelig for døve og tunghørte.
  - Hvis man ikke har noen hender ledig til å holde boken man leser, for eksempel hvis man er **ute og løper**, så vil det være praktisk å lese lydboka istedenfor. Det samme er tilfellet hvis man har en funksjonsnedsettelse som gjør det vanskelig å bruke henda.
  - Hvis man prøver å **lære seg et nytt språk eller fagfelt**, så kan det være greit å både høre og se teksten samtidig for å lære hvordan ordene høres ut.

6. Før vi begynner å se på kildekode så kan jeg raskt nevne litt bakgrunnsstoff hvis noen vil gå litt mer i dybden senere.
  - WCAG 2.0 er gode retninglinjer for å lage tilgjengelige nettsider, og vi er pålagt å følge denne standarden når vi lager nettsider i Norge. Siden EPUB i et nøtteskall er en spesifikasjon som beskriver hvordan man skal lagre en nettside inni en ZIP-fil, så er dette retningslinjer vi bør følge også når vi lager e-bøker.
  - WAI-ARIA er også en viktig standard, men er viktigst i sammenhenger hvor innholdet endrer seg dynamisk. Det kan være aktuelt i lærebøker hvor man sender inn svar på oppgaver og i barnebøker med interaktivitet.
  - Noen bøker det kan være verdt å se på er "EPUB 3 Best Practices", "EPUB 3 Accessibility Guidelines", og "Web og Universell utforming". Dere kan søke de opp på nett.
  - "Løsningsforslag for web", utformet av Difi - Direktoratet for forvaltning og IKT. Her ligger det mye konkret informasjon om hvordan innhold kan merkes opp. Det er en veldig god ressurs som jeg varmt kan anbefale, og som jeg kommer til å hente litt fra videre i denne presentasjonen.

7. Skill mellom innhold og utseende
  - Det visuelle uttrykket er ofte det eneste e-bok-forfattere tar hensyn til når de produserer innhold.
  - Når man produserer en e-bok er det viktig å tenke på at ikke alle kommer til å bruke boken på samme måte.
  - Noen vil bruke en skjermleser for å få boken lest opp eller vist på en leselist.
  - For å navigere i boken vil mange e-bok-lesere basere seg på hvordan innholdet i boken er markert opp.
  - Dessuten vil man at boka skal vises litt forskjellig hvis man skriver den ut på papir.
  - Og en godt oppmerket bok gjør det enkelt å produsere en lydbok-versjon og en punktskrift-versjon av boka, mer eller mindre automatisk.

8. Bruk riktige elementer
  - hvis du trenger en liste, bruk liste-elementene
  - hvis du trenger en tabell, bruk tabell-elementene

9. Det må være tydelig forskjell mellom overskrifter av ulike nivå
  - I denne innholdsfortegnelsen refereres det til en overskrift på øverste nivå; nivå 1, flere overskrifter på nivå 2, og et par overskrifter på nivå 3.

10. (forts) Overskrifter på ulike nivå
  - Tilsvarende i selve innholdet så må overskriften på nivå 1 markeres opp med HTML-taggen `h1`, overskriften på nivå 2 må markeres opp med HTML-taggen `h2`, og så videre.
  - Jeg har sett eksempler der alt i boken er markert opp som avsnitt, til og med overskriften. Jeg har også sett eksempler på at overskriftene er bilder.
  - Hvis overskriftene ikke merkes opp som overskrifter, så vil det ikke være mulig å navigere mellom kapitler når man navigerer med tastaturet, eller hvis man bruker innholdsfortegnelsen som blir generert av noen lesesystemer.

13. Fargebruk og kontrast (visuelle eksempler på god og dårlig kontrast i presentasjonen)
  - Det finnes mange gode verktøy på nett for å teste kontraster.

14. Språk
  - Hvis det brukes flere språk i teksten så kan `lang`-attributten brukes for å si hvilket språk teksten er på.
  - Dette er viktig for at en talesyntese skal kunne lese teksten med riktig språk.

16. Sekundært innhold
  - Bøker har en hovedfortelling som leserne forventes å følge fra begynnelse til slutt, og det er viktig å kunne navigere uavbrutt i denne fortellingen.
  - De fleste bøker inneholder en viss grad av supplerende opplysninger blandet inn i hovedfortellingen.
  - For eksempel sidetall, fotnoter, referanser, faktabokser, tabeller, figurer, diagrammer og lignende.
  - Disse elementene må være markert opp på en måte som indikerer at det ikke er en del av hovedfortellingen.
  - Hvis dette er gjort riktig, så kan den som leser boka enkelt velge å for eksempel hoppe over store tabeller og figurer med detaljerte beskrivelser.

8. epub:type
  - HTML har et relativt begrenset sett med elementer.
  - Det kan for eksempel være hundrevis med `aside`-elementer, men man kan ikke med HTML angi forskjellen på en fotnote og en faktaboks.
  - EPUB 3 har introduserte `epub:type`-attributten.
  - Med denne kan man plukke verdier fra et standard-vokabular for å angi at et element representerer for eksempel et sideskift, eller en info-boks.

10. Bilder
  - Alle bilder må ha en `alt`-attributt.
  - Ikke legg filnavnet i `alt`-attributtet.
  - `title`-attributtet bør ikke brukes, da det hverken er tilgjengelig for skjermlesere eller for touch-skjerm-brukere.
  - Hvis et bilde kun er dekorativt og ikke meningsbærende, så må `alt`-attributten være tom.
  - Bilder som er en del av innholdet må ha en beskrivende tekst i `alt`-attributtet.

11. Fotnoter
  - Notereferanser og fotnoter skal merkes med henholdsvis "noteref" og "footnote".
  - Mange vil kanskje ikke høre fotnotene med en gang.

12. Synkronisert tekst og lyd (eksempel; video? eller embeddet i presentasjonen? HTML-presentasjon?)
  - "EPUB-bøker kan inneholde en kombinasjon av lyd, tekst og bilder."
  - Synkronisert tekst og lyd kan eksempelvis være nyttig ved lesetrening.

13. Metadata
  - Det lønner seg å produsere universelt utformede e-bøker. I metadata kan man deklarere hvor tilgjengelig boken er.
  - For eksempel så kan man si:
    + index - at boken inneholder et register
    + printPageNumbers - at sidenummerering fra papir-versjonen er med
    + structuralNavigation - at boken har markert opp overskrifter på riktig måte
    + unlocked - at boken er uten DRM
    + alternativeText - at alle bilder bruker `alt`-attributten på riktig måte
  - Dette er informasjon som med fordel kan gjøres tilgjengelig for kunder i en nettbokhandel eller i biblioteker når de bestiller en bok.
  - For eksempel kunne en kunde søkt etter bøker som har visse egenskaper.
  - Kanskje man er interessert i en e-bok-versjon av en studiebok, men bare hvis den har sidetallene fra papir-versjonen lagt inn i seg.
  - Hvis man skal velge seg en bok å lese så har man med god metadata en mulighet til å sammenligne den tekniske kvaliteten på disse før man kjøper eller låner.

14. Hva NLB ønsker fra forlag
  - Vi i NLB ønsker oss fortrinnsvis EPUB. Vi kan også godta InDesign- eller Word-filer, og til-og-med PDF-filer (helst PDF/UA eller PDF/A), men vi bruker EPUB i produksjonssystemene våre når vi leser inn lyd eller konverterer til punktskrift.
  - Dagens situasjon for bøker hvor vi ikke får filer fra forlag er at vi kjøper inn den fysiske boka, kutter den opp, og skanner inn alle sidene som PDF. Deretter bruker vi eksterne leverandører for å gjøre om disse PDFene til EPUB. Hvis vi får EPUB direkte fra forlag så slipper vi dette ekstraarbeidet.



