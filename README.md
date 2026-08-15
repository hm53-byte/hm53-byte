# hm53-byte

Kazalo javnih repozitorija.

Autor je student prava i gradi alate za rad s hrvatskim pravnim i
registarskim izvorima. Dio repozitorija je cjelovit kod, dio je izlog
zatvorenog sustava: opis arhitekture, mjerene brojke i jedan modul objavljen
u cijelosti. Gdje je tako, u naslovu repozitorija pise izlog.

Sve brojke o testovima izmjerene su pokretanjem, a datum mjerenja stoji u
svakom repozitoriju. Izlozi navode i sto citatelj moze provjeriti sam, a sto
ne moze jer dolazi iz zatvorenog repozitorija.

---

## Cjeloviti alati

**[croatian-case-law](https://github.com/hm53-byte/croatian-case-law)**
Lokalni korpus hrvatske sudske prakse sa SQLite bazom, FTS5 indeksom i
hibridnom pretragom, za istrazivanje prakse bez mreznih zahtjeva.

**[LEGAL-SUITE](https://github.com/hm53-byte/LEGAL-SUITE)**
Streamlit aplikacija koja iz web forme popuni predlozak hrvatskog pravnog
podneska ili ugovora i vrati .docx, za osobu koja vec zna koji dokument treba.
82 generatora u 18 modula.

**[croatian-registry-pipeline](https://github.com/hm53-byte/croatian-registry-pipeline)**
Cjevovod koji prikuplja objave iz hrvatskih javnih registara i spaja entitete
po identifikatoru pravne osobe i katastarskoj cestici. Ugradjene samoprovjere
cuvaju negativan nalaz: kad test padne, mijenja se opis, ne test.

**[DOSJE](https://github.com/hm53-byte/DOSJE)**
Kostur alata koji usporedjuje zemljisnoknjizni i katastarski zapis o istoj
cestici i razrjesava vezu medju njima. Mjerenje na 100 cestica podiglo je
spojivost s 0,60 na 0,86.

**[padic-address-index](https://github.com/hm53-byte/padic-address-index)**
Hijerarhijsko suzavanje nad hrvatskim sudskim spisima prije semantickog
dohvata. Adresa od pet clanova i ultrametrika umjesto euklidske udaljenosti,
pa su skupine ili disjunktne ili ugnijezdene, nikad djelomicno preklopljene.
332 retka bez ovisnosti, 47 testova.

**[extraction-guards](https://github.com/hm53-byte/extraction-guards)**
Kako provjeriti izlaz ekstrakcije bez oznacenog skupa i bez drugog modela.
Dodavanje poznate kolicine mjeri tocnost, metamorficka proba mjeri stabilnost,
a pet kanala koji s modelom ne dijele nacin otkazivanja provjerava pojedini
odgovor. Nijedna proba sama nije dovoljna: naivni ekstraktor koji grijesi u
svih 50 slucajeva prolazi metamorficku probu 9 od 9. 36 testova.

**[sink-gate](https://github.com/hm53-byte/sink-gate)**
Staticka AST provjera koja hvata modul koji radi posao a rezultat mu nikamo ne
tece, i modul koji prekoracuje svoj sloj. Nije mrtav kod u uobicajenom smislu:
uvozi se, ima testove i testovi prolaze. Bez ovisnosti, 15 testova, primjer s
oba kvara ukljucen.

**[reality-ground](https://github.com/hm53-byte/reality-ground)**
Provjeri mehanicki postoji li funkcija, tablica ili modul vec u kodu prije
nego ga napises. Nastalo iz dva propusta u istoj veceri, oba zapisana.

## Izlozi zatvorenih sustava

**[registry-distress-monitor](https://github.com/hm53-byte/registry-distress-monitor)**
Vremenski nadzor javnih registara koji trazi rani znak da subjekt ulazi u
nevolju. 41k redaka, 2089 testova. Tri zadrzana negativna nalaza, ukljucujuci
signal koji se pokazao losijim od slucajnog. Modul konformne kalibracije
objavljen u cijelosti.

**[law-office-toolkit](https://github.com/hm53-byte/law-office-toolkit)**
Lokalna infrastruktura za mali odvjetnicki ured: spisi, rokovi, sukob
interesa, pretraga vlastitog korpusa, jezicni model na uredskom racunalu. 51k
redaka, 965 testova. Mrezna straza objavljena u cijelosti.

**[nfc-ordering-system](https://github.com/hm53-byte/nfc-ordering-system)**
Sustav narucivanja dodirom telefona za ugostiteljstvo. 49k redaka bez ijedne
vanjske ovisnosti, 1315 testnih metoda, migracije s verzijom u zaglavlju same
datoteke baze. Brava nad bazom objavljena u cijelosti.

**[sector-lead-engine](https://github.com/hm53-byte/sector-lead-engine)**
Cjevovod koji iz javnih izvora sastavlja sektorski popis subjekata. 390
testova, zatvorena brana pred svakim kolektorom. Bijeli popis polja koji brani
da osobni podaci udju u bazu objavljen je u cijelosti.

**[scout-platform](https://github.com/hm53-byte/scout-platform)**
Platforma za nogometni skauting, izvan pravne domene. 29k redaka, 363 testa,
trajna pohrana nad posluziteljem koji gubi zapise i dvosmjerni sync s
rjesavanjem sukoba.

---

## Kroz sve projekte

Nekoliko stvari ponavlja se svjesno, i lakse ih je vidjeti odjednom nego po
repozitorijima.

**Smjer greske se bira unaprijed.** Bijeli popis umjesto crnog, zatvorena
brana kad se izvor ne moze provjeriti, nepoznat oblik adrese koji se odbija
umjesto propusta. Skuplja je tiha pogreska od glasne.

**Negativan nalaz se cuva.** Signal koji je mjeren kao beskoristan, ubrzanje
koje vrijedi samo u jednom rezimu, put u kodu koji obecava sazimanje a ne
sazima. Sve troje stoji zapisano uz test koji ga pribija.

**Brojka nosi datum i nacin mjerenja**, ili se ne navodi.

---

Index of public repositories. Complete tools: a local corpus of Croatian case
law with FTS5 and hybrid search; a Streamlit generator of Croatian legal
documents; a public-registry collection
pipeline whose CI tests protect a negative finding; a land-registry and
cadastre reconciliation skeleton; an ultrametric hierarchical index for court
case numbers; label-free probes and non-circular channels for extraction
quality; a static AST gate for modules whose output never reaches a sink; and a
tool that checks whether a symbol already exists before you write it.

Showcases of closed systems, each with measured figures and one module
published in full: a temporal distress monitor over public registries (2089
tests, conformal prediction module); a local law-office toolkit (965 tests,
socket-level network guard); an NFC ordering system with zero external
dependencies (1315 test methods, single-writer lock); a sector lead pipeline
(390 tests, GDPR whitelist scrubber); and a football scouting platform
(363 tests, two-way sync with conflict retention).

The author is a law student building tools for Croatian legal and registry
sources.
