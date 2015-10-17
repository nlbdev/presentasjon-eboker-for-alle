e-bøker for alle
================


1. E-bøker for alle!
    Hei, jeg heter Jostein og kommer fra Norsk lyd- og blindeskriftbibliotek, og jeg vil fortelle litt om hvordan dere kan produsere bøker på en måte som gjør de tilgjengelige for så mange mennesker som mulig.
2. Kort om NLB
  - Vi gjør bøker tilgjengelige for mennesker med lesevansker. Åndsverkloven § 17a åpner for at [vi kan lage lydbøker til bruk for funksjonshemmede](http://www.nlb.no/om-nlb/fakta/organisasjonen/lovgrunnlag-aandsverkloven-17a/) uten å innhente samtykke fra rettighetshaveren på forhånd. [Lydbokavtalen](http://www.kopinor.no/rettighetshavere/individuelt-vederlag/lydboker/dokumenter/lydbokavtalen) fastsetter vilkårene for eksemplarfremstilling, distribusjon og vederlag. Med dette i ryggen kan vi produsere og distribuere et variert tilbud av lyd- og punktskrift-bøker. Vi produserer skjønnlitteratur og sakprosa for både barn, ungdom og voksne. I tillegg produserer vi studielitteratur for studenter ved høyere utdanning.
- Vi er alle utsatt for situasjonsbetingte lesevansker `[4]` (bruk bilder for å illustrere hver av disse situasjonene)
  - Hvis man leser på en mobiltelefon så har man kun tilgang til en liten porsjon tekst om gangen, akkurat som mennesker som zoomer mye på en datamaskin fordi de ser dårlig, og akkurat som blinde som bruker leselist.
  - Hvis man leser ute i sola så vil man oppleve problemer med kontraster
  - Hvis man sitter på toget og ser en video så vil man kanskje skru på undertekster for å ikke forstyrre andre, på samme måte som en døv person ville gjort det
  - Hvis det er for mørkt til å lese, eller hvis man ikke har noen hender ledig til å holde boka, så vil man kanskje sette pris på å kunne veksle mellom lyd-versjonen og tekst-versjonen av boka
  - Hvis man prøver å lære å lese et språk, så kan det være greit å både høre og se teksten samtidig

> Statistisk sentralbyrå har funnet ut at det er omtrent 17 % av norges befolkning mellom 16 og 66 år som har registrert en form for funksjonsnedsettelse, enten midlertidig eller varig. Dette utgjør omtrent 500 000 mennesker i Norge.
>
> Eksperiment: reis dere (eller rekk opp hånden?) hvis du enten:
> - har hørselsproblemer
> - er blind
> - er fargeblind
> - har dysleksi
> - bruker briller eller kontaktlinser
> - har adhd
> - har vært gravid
> - har brukket en arm eller et bein (og har gips pga det)
> - har vært full noen gang
> - ikke har norsk som primærspråk
> - er trøtt fordi man har vært oppe med småbarn om natten
> 
> Universell utforming er altså viktig ikke bare for de som har en "registrert" funksjonsnedsettelse men for de aller aller fleste.

- WCAG 2.0 er gode retninglinjer, og vi er pålagt å følge denne standarden i Norge
- WAI-ARIA er også en viktig standard, men er viktigst i sammenhenger hvor innholder endrer seg dynamisk
- Tekst og struktur `[3]` `[4]`
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


