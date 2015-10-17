e-bøker for alle
================


1. E-bøker for alle!
    Hei, jeg heter Jostein og kommer fra Norsk lyd- og blindeskriftbibliotek, og jeg vil fortelle litt om hvordan dere kan produsere bøker på en måte som gjør de tilgjengelige for så mange mennesker som mulig.
2. Kort om NLBj (TODO: illustrasjon av "lydbok" og "punktbok", TODO: illustrasjon av "alle aldre")
  - Vi er et offentlig bibliotek som produserer og låner ut lydbøker og punktskriftbøker.
  - Tilbudet er for alle som strever med å lese trykt tekst, enten det skyldes dysleksi, synsvansker eller andre funksjonsnedsettelser som gjør det vanskelig å lese.
  - Vi har lånere fra hele landet, og tilbudet er gratis.
  - Vi produserer skjønnlitteratur og sakprosa for både barn, ungdom og voksne.
  - I tillegg produserer vi studielitteratur for studenter ved høyere utdanning.
3. Universell utforming (TODO: trenger illustrasjon)
  - Universell utforming betyr at *"hovedløsningen"* skal benyttes av flest mulig.
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
  - Hvis man sitter **på toget eller bussen** og leser en nettavis så vil mange unngå å se videoer de kommer over i nyhetsartikler for å ikke forstyrre medpassasjerene. Hvis videoen hadde hatt undertekster så ville det vært greit å se videoen med lyden avslått. Dette ville også gjort videoen mer tilgjengelig for døve og tunghørte.
  - Hvis man ikke har noen hender ledig til å holde boken man leser, for eksempel hvis man er **ute og løper**, så vil det være praktisk å lese lydboka istedenfor. Det samme er tilfellet hvis man har en funksjonsnedsettelse som gjør det vanskelig å bruke henda.
  - Hvis man prøver å **lære seg et nytt språk eller fagfelt**, så kan det være greit å både høre og se teksten samtidig for å lære hvordan ordene høres ut.
6. Før vi begynner å se på kildekode så kan jeg raskt nevne litt bakgrunnsstoff hvis noen vil gå litt mer i dybden senere.
  + WCAG 2.0 er gode retninglinjer, og vi er pålagt å følge denne standarden når vi lager nettsider i Norge. Siden e-bøker i praksis er "en nettside i en ZIP-fil" så er dette regningslinjer vi bør følge også når vi lager e-bøker.
  + WAI-ARIA er også en viktig standard, men er viktigst i sammenhenger hvor innholder endrer seg dynamisk. Det kan være aktuelt i lærebøker hvor man sender inn svar på oppgaver og i barnebøker med interaktivitet.
  + Noen bøker det kan være verdt å se på er "EPUB 3 Best Practices", "EPUB 3 Accessibility Guidelines", og "Web og Universell utforming". Dere kan søke de opp på nett.
  + "Universell Utforming-skolen for nettsider" er en nettside utviklet av Difi - Direktoratet for forvaltning og IKT. Det er en veldig god ressurs som jeg varmt kan anbefale, og som jeg kommer til å hente litt fra videre i denne presentasjonen.
7. Tekst og struktur `[3]` `[4]`
- epub:type `[4]`
- Skille innhold og presentasjon `[3]` `[4]`
  - `<em>`, `<strong>`, `<i>` og `<b>` kontra `font-style: italic` og `font-weight: bold` `[4]`
- Bilder og grafikk `[3]` `[4]`
- Tabeller `[3]` `[4]`
- Fotnoter `[4]`
- Fargebruk og kontrast `[3]` (visuelle eksempler på god og dårlig kontrast i presentasjonen)
- Språk i koden `[3]` `[4]`
- Leserekkefølge `[4]` (grafisk fremstilling av leserekkefølgen på en eller annen måte? tegne piler over teksten?)
- Sekundært innhold (bruke f.eks. `<figure>` for å markere innhold som ikke tilhører det primære innholdet / hovedfortellingen) `[4]`
- Synkronisert tekst og lyd (eksempel; video? eller embeddet i presentasjonen? HTML-presentasjon?)
- Metadata
  - Det lønner seg å produsere universelt utformede e-bøker. I metadata kan man deklarere hvor tilgjengelig boken er.
    For eksempel, hvorvidt boken inneholder tekst-alternativ for bilder og illustrasjoner, om matematiske og kjemiske formler
    er tilgjengelige, om sidenummerering er inkludert, om innlest synkronisert lyd er inkludert, og så videre. Dette er informasjon
    som med fordel kan gjøres tilgjengelig for kunder i en nettbokhandel eller i biblioteker når de bestiller en bok.
- Hva NLB ønsker fra forlag
  - Vi i NLB ønsker oss fortrinnsvis EPUB. Vi kan også godta InDesign- eller Word-filer, og til-og-med PDF-filer (helst PDF/UA eller PDF/A), men vi bruker EPUB i produksjonssystemene våre når vi leser inn lyd eller konverterer til punktskrift.
  - Dagens situasjon for bøker hvor vi ikke får filer fra forlag er at vi kjøper inn den fysiske boka, kutter den opp, og skanner inn alle sidene some PDF. Deretter bruker vi eksterne leverandører for å gjøre om disse PDFene til EPUB. Hvis vi får EPUB direkte fra forlag så slipper vi dette ekstraarbeidet.

Noen ting som antagelig blir gjennomgått i presentasjonen før meg:
- EPUB er ikke hovedsakling en spesifikasjon for å markere opp innhold, det er et *publikasjonsformat*. Det er på mange måter "en nettside i en zip-fil".
- Sidenummer `[4]`

--------------------

TODO:
- Bruke som bakgrunnsfarge: `abdae4`
- Få inn NLBs logo et sted

*[Wikipedia om universell utforming](https://no.wikipedia.org/wiki/Universell_utforming)*:
> Universell utforming skiller seg fra tilgjengelighet ved at den ikke krever spesialløsninger for enkeltgrupper,
som for eksempel egen inngang for rullestoler. I en universelt utformet løsning er det hovedløsningen som skal være brukbar for alle.

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

