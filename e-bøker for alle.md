e-bøker for alle
================


1. E-bøker for alle!
    Hei, jeg heter Jostein og kommer fra Norsk lyd- og blindeskriftbibliotek, og jeg vil fortelle litt om hvordan dere kan produsere bøker på en måte som gjør de tilgjengelige for så mange mennesker som mulig.

2. Litt kort om NLB først (TODO: illustrasjon av "lydbok" og "punktbok", TODO: illustrasjon av "alle aldre")
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
  - Jeg vil tro dette gjelder alle her. Vi har alle hatt en funksjonsnedsettelse på et eller annet tidspunkt.
  - Universell utforming er altså viktig ikke bare for de som har en *"registrert"* funksjonsnedsettelse men for de aller aller fleste.

5. I tillegg så er vi alle utsatt for funskjonshemninger, eller *situasjonsbetingte lesevansker*
  - Hvis man leser på en **mobiltelefon** så har man kun tilgang til en liten porsjon tekst om gangen. Da har man den samme utfordringen som de som ser dårlig og trenger å forstørre teksten på PC-skjermen. Det er også samme utfordring som de som er blinde har når de leser punktskrift.
  - Hvis det blir for **mørkt** til å lese, så vil man kanskje sette pris på å kunne veksle mellom tekst-versjonen av boka og lydboka. Da har man den samme utfordringen som de som er tilnærmet eller helt blinde.
  - Hvis man leser ute **i sola** så vil man oppleve problemer med kontraster. Det er stor variasjon i lysforhold og skjermkvalitet der folk leser. God kontrast er viktig for folk med fargeblindhet og for de med nedsatt kontrastfølsomhet, som vanligvis følger med aldring.
  - Hvis man sitter **på toget eller bussen** og leser en nettavis så vil mange kanskje unngå å se videoer de kommer over i nyhetsartikler for å ikke forstyrre medpassasjerene. Hvis videoen hadde hatt undertekster så ville det vært greit å se videoen med lyden avslått. Dette ville også gjort videoen mer tilgjengelig for døve og tunghørte.
  - Hvis man ikke har noen hender ledig til å holde boken man leser, for eksempel hvis man er **ute og løper**, så vil det være praktisk å lese lydboka istedenfor. Det samme er tilfellet hvis man har en funksjonsnedsettelse som gjør det vanskelig å bruke henda.
  - Hvis man prøver å **lære seg et nytt språk eller fagfelt**, så kan det være greit å både høre og se teksten samtidig for å lære hvordan ordene høres ut.

6. Før vi begynner å se på kildekode så kan jeg raskt nevne litt bakgrunnsstoff hvis noen vil gå litt mer i dybden senere.
  - WCAG 2.0 er gode retninglinjer for å lage tilgjengelige nettsider, og vi er pålagt å følge denne standarden når vi lager nettsider i Norge. Siden EPUB i et nøtteskall er en spesifikasjon som på en måte beskriver hvordan man skal lagre en nettside inni en ZIP-fil, så er dette retningslinjer vi bør følge også når vi lager e-bøker.
  - WAI-ARIA er også en viktig standard, men er viktigst i sammenhenger hvor innholdet endrer seg dynamisk. Det kan være aktuelt i lærebøker hvor man sender inn svar på oppgaver og i barnebøker med interaktivitet.
  - Noen bøker det kan være verdt å se på er "EPUB 3 Best Practices", "EPUB 3 Accessibility Guidelines", og "Web og Universell utforming". Dere kan søke de opp på nett.
  - "Løsningsforslag for web", utformet av Difi - Direktoratet for forvaltning og IKT. Her ligger det mye konkret informasjon om hvordan innhold kan merkes opp. Det er en veldig god ressurs som jeg varmt kan anbefale, og som jeg kommer til å hente litt fra videre i denne presentasjonen.
  - TODO: bør si noe om lite tilgjengelige nettbutikker her kanskje? Vanskelig å kjøpe bøker.

7. Det må være tydelig forskjell mellom overskrifter av ulike nivå
  - I denne innholdsfortegnelsen refereres det til en overskrift på øverste nivå; nivå 1, flere overskrifter på nivå 2, og et par overskrifter på nivå 3.

8. (forts) Overskrifter på ulike nivå (TODO: ikke glidende animasjon mot neste slide)
  - Tilsvarende i selve innholdet så må overskriften på nivå 1 markeres opp med HTML-taggen `h1`, overskriften på nivå 2 må markeres opp med HTML-taggen `h2`, og så videre.
  - Jeg har sett eksempler der alt i boken er markert opp som avsnitt, til og med overskriften. Jeg har også sett eksempler på at overskriftene er bilder.
  - Hvis overskriftene ikke merkes opp som overskrifter, så vil det ikke være mulig å navigere mellom kapitler når man navigerer med tastaturet, eller hvis man bruker innholdsfortegnelsen som blir generert av noen lesesystemer.

9. Skille innhold og presentasjon
  - Det visuelle uttrykket er ofte det eneste e-bok-forfattere tar hensyn til når de produserer innhold.
  - Ved 

9. Skille innhold og presentasjon `[4]`
  - `<em>`, `<strong>`, `<i>` og `<b>` kontra `font-style: italic` og `font-weight: bold` `[4]`

8. epub:type `[4]`
  - epub:type
  - Sidenummer `[4]`

10. Bilder `[4]`

11. Tabeller `[4]`

12. Fotnoter `[4]`

13. Fargebruk og kontrast (visuelle eksempler på god og dårlig kontrast i presentasjonen)

14. Språk `[4]`
  - Hvis det brukes flere språk i teksten så kan lang attributten si ifra til talesyntesen at den skal bruke riktig språk til å lese høyt

15. Leserekkefølge `[4]` (grafisk fremstilling av leserekkefølgen på en eller annen måte? tegne piler over teksten?)
  - Bøker har en hovedfortelling som leserne forventes å følge fra begynnelse til slutt, og det er viktig å kunne navigere uavbrutt i denne fortellingen.
  - De fleste bøker inneholder en viss grad av supplerende opplysninger blandet inn i hovedfortellingen.
  - For eksempel sidetall, fotnoter, referanser, faktabokser, tabeller, figurer, diagrammer og lignende.
  - Disse elementene må være markert opp på en måte som indikerer at det ikke er en del av hovedfortellingen.
  - Hvis dette er gjort riktig, så kan den som leser boka enkelt velge å for eksempel hoppe over store tabeller og figurer med detaljerte beskrivelser.
  - 

16. Sekundært innhold (bruke f.eks. `<figure>` for å markere innhold som ikke tilhører det primære innholdet / hovedfortellingen) `[4]`

17. Synkronisert tekst og lyd (eksempel; video? eller embeddet i presentasjonen? HTML-presentasjon?)

18. Metadata
  - Det lønner seg å produsere universelt utformede e-bøker. I metadata kan man deklarere hvor tilgjengelig boken er.
    For eksempel, hvorvidt boken inneholder tekst-alternativ for bilder og illustrasjoner, om matematiske og kjemiske formler
    er tilgjengelige, om sidenummerering er inkludert, om innlest synkronisert lyd er inkludert, og så videre. Dette er informasjon
    som med fordel kan gjøres tilgjengelig for kunder i en nettbokhandel eller i biblioteker når de bestiller en bok.

19. Hva NLB ønsker fra forlag
  - Vi i NLB ønsker oss fortrinnsvis EPUB. Vi kan også godta InDesign- eller Word-filer, og til-og-med PDF-filer (helst PDF/UA eller PDF/A), men vi bruker EPUB i produksjonssystemene våre når vi leser inn lyd eller konverterer til punktskrift.
  - Dagens situasjon for bøker hvor vi ikke får filer fra forlag er at vi kjøper inn den fysiske boka, kutter den opp, og skanner inn alle sidene some PDF. Deretter bruker vi eksterne leverandører for å gjøre om disse PDFene til EPUB. Hvis vi får EPUB direkte fra forlag så slipper vi dette ekstraarbeidet.

--------------------

TODO:
- Bruke som bakgrunnsfarge: `abdae4`
- Få inn NLBs logo et sted

Litt bakgrunnsstoff:
 1. [EPUB 3 Best Practices](http://shop.oreilly.com/product/0636920024897.do)
 2. [Web og Universell Utforming](http://www.universitetsforlaget.no/nettbutikk/web-og-universell-utforming-uf.html)
 3. [uu-skolen for nettsider](http://uu.difi.no/veiledning/nettsider/uu-skolen/bilder-og-grafikk)
 4. [EPUB 3 Accessibility Guidelines](http://www.idpf.org/accessibility/guidelines/)

Note to self:

- prøv å bruk "nudges"
  - få forlag og e-bokprodusenter til å inkludere alt-tekster på bilder
  - få forlag til å inkludere metadata om tilgjengelighet

NLBs fargekoder:
- Gul: `fff218`
- Brun: `e1962f`
- Oransje: `f37031`
- Rød: `c32123`
- Magenta: `dc0099`
- Lilla: `c129d2`
- Blå: `00bbe4` - med 25% saturation istedenfor 100%: `abdae4`
- Lysegrønn: `a6ce39`
- Mørkegrønn: `0d8204`

