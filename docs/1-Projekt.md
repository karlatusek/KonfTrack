# 1. Opseg projekta

**Cilj:** Organizacija znanstvene konferencije koja se sastoji od objava informacija o konferenciji, primanje znanstvenih radova, dodjele recenzenata, provođenje recenzijskog postupka, donošenje odluka o prihvaćanju radova i izrada programa konferencije. Korisnici su: sudionici konferencija, recenzenti, autori radova i organizatori konferencija.

## 1.1 Problem i cilj projekta

**Cilj:** Cilj projekta KonfTrack je razviti web-platformu koja omogućuje upravljanje znanstvenim konferencijama i njihovim ključnim organizacijskim procesima. Sustav će podržavati upravljanje korisnicima i njihovim pravima pristupa, stvaranje i uređivanje konferencija, predaju znanstvenih radova, dvostruko slijepo recenziranje, donošenje odluka te organizaciju programa konferencije. Također će omogućiti slanje obavijesti povezanih s važnim događajima u postupku organizacije konferencije u slučaju promjena.

Organizacija znanstvenih konferencija često se oslanja na razmjenu e-mailova i sinkronizaciju tablica. Takav pristup dovodi do gubitka dokumenata, propuštanja strogih rokova, rizika od curenja identiteta autora tijekom recenzije te otežane komunikacije između organizatora, recenzenata i autora.

Očekivana korist projekta je jednostavnije upravljanje konferencijama, bolja preglednost tijeka obrade radova, lakše praćenje rokova i jasnije razdvajanje ovlasti među sudionicima. Sustav bi trebao omogućiti da autori, recenzenti i organizatori pristupaju funkcijama i informacijama koje su im potrebne, uz očuvanje povjerljivosti recenzijskog postupka i zaštitu osobnih podataka.



## 1.2 Ciljani korisnici i dionici

**Cilj:** Utvrditi osobe, uloge i organizacije čije potrebe i interesi određuju projektni zadatak.

| Skupina korisnika ili dionika | Potreba ili interes relevantan za ovaj projekt |
| --- | --- |
| Administrator sustava | Upravljanje korisničkim računima i provođenje administrativnih aktivnosti |
| Autor rada | Pregledati dostupne konferencije, predati rad, upravljati vlastitim predajama u dopuštenom razdoblju i pregledati dostupne informacije o odlukama |
| Recenzent | Pregledati dodijeljene radove te izraditi i predati recenziju u propisanom roku |
| Organizator konferencije | Pratiti tijek recenziranja, vidjeti rezultate recenzija, donositi odluke i organizirati program konferencije u skladu s dodijeljenim ovlastima |
| Korisnici | Prijava na konferencije i sigurnost podataka |

Korisničke uloge definiraju se prema potrebama sustava. Pojedini korisnik može sudjelovati u više konferencija, a njegova prava pristupa mogu ovisiti o ulozi dodijeljenoj za određenu konferenciju.
<details>
<summary><strong>Korisnici, dionici i neobavezna persona</strong></summary>

**Primjer — CrisisMap:**

| Skupina korisnika ili dionika | Potreba ili interes relevantan za ovaj projekt |
| --- | --- |
| Građanin | Pronaći informacije o obližnjim kriznim događajima i podnijeti prijavu kriznog događaja s lokacijom. |
| Koordinator pomoći | Pregledati prijave relevantne za područje i dostupne resurse, ako je koordinacija unutar odobrenog opsega. |
| Regulatorno tijelo / Agencija za zaštitu podataka (Dionik) | Zahtijeva osiguravanje anonimnosti prijavitelja i zaštitu osobnih podataka (npr. usklađenost s GDPR-om). Ovaj dionik ne koristi aplikaciju, ali definira ograničenja sustava. |

Riječ je o dvjema različitim potrebama, a ne o dvjema izmišljenim biografijama. Akter komunicira s aplikacijom; demonstrator na kolegiju kojem je rezultat zanimljiv ne mora biti akter aplikacije. Koristite uloge i ovlasti iz svojeg odobrenog zadatka. Persona je neobavezna i korisna je kada pomaže riješiti konkretno projektno pitanje.

**Neobavezni primjer persone:** Ana, koordinatorica pomoći, treba aktualne informacije o resursima kako bi mogla rasporediti pomoć. To može pomoći kada tim odlučuje koje informacije koordinator treba vidjeti prve. Personu opišite samo ako objašnjava projektnu odluku; popis izmišljenih biografija nije obavezni rezultat kolegija.

</details>

## 1.3 Granice projekta

**Cilj:** Jasno definirati granice sustava — što je obuhvaćeno odobrenim zadatkom, što je svjesno izostavljeno ili odgođeno te o kojim vanjskim uslugama sustav izravno ovisi.

**Uključeno:** 

->Registracija korisnika, prijava, odjava, upravljanje profilom i promjena lozinke.

->Definiranje korisničkih uloga i provjera prava pristupa na backendu.

->Stvaranje, pregled i uređivanje konferencija te upravljanje njihovim statusima, vidljivošću, znanstvenim temama i rokovima.

->Predaja znanstvenih radova, pohrana njihovih datoteka i upravljanje statusima predaja.

->Provođenje dvostruko slijepog recenziranja, dodjela recenzenata i evidentiranje recenzija.

->Evidentiranje odluka o radovima i obavještavanje korisnika o važnim događajima.

->Validacija ulaznih podataka


**Izvan opsega ili odgođeno:** 

->Automatizirano generiranje i objavljivanje cjelovitih zbornika radova, osim ako se ta funkcionalnost naknadno potvrdi kao dio obveznog opsega.

->Napredne integracije s vanjskim sustavima, primjerice Crossrefom ili ORCID-om, jer nisu uključene u odobreni zadatak.

->Integracija s vanjskim sustavima za plaćanje kotizacija, jer nije dogovorena kao zahtjev projekta.

->Napredne funkcionalnosti koje nisu potrebne za ostvarenje osnovnih procesa upravljanja konferencijama.


**Vanjske ovisnosti:** 

->Sustav za upravljanje relacijskom bazom podataka za pohranu korisnika, konferencija, radova, recenzija i povezanih podataka. ()

->Poslužiteljsko okruženje za pokretanje web-aplikacije i pohranu datoteka. ()

->Usluga za slanje obavijesti putem e-pošte i postupak resetiranja lozinke. ()

->Vanjski pružatelj identiteta (OAuth)

->Sustav za verzije koda i suradnju na projektu. (GitHub)


<details>
<summary><strong>Primjer početne granice projekta</strong></summary>

**Primjer — CrisisMap:**  
**Uključeno:** Podnošenje prijave kriznog događaja s lokacijom i pregled prijava na karti.  
**Isključeno:** Automatsko angažiranje hitnih službi; prikaz prijave ne odobrava niti pokreće službenu intervenciju.  
**Vanjska ovisnost:** Pružatelj kartografskih usluga omogućuje prikaz karte; aplikacija ostaje odgovorna za vlastite podatke o prijavama.

Ovo je konkretna granica jer razdvaja prikaz informacija od službenog odgovora hitnih službi i određuje koji sustav osigurava kartu. Izuzeće i ovisnost dio su **nastavnog scenarija**, a ne tvrdnja o tome što objavljena aplikacija stvarno implementira; te činjenice određuju odobreni opseg i stvarna aplikacija tima.

**Drugi primjer korisne granice:** U prvoj implementaciji usredotočite se na koordinaciju odgovora na poplavu. Navedite vrste događaja ili korisnika koje pokriva odobreni projekt umjesto obećavanja svih mogućih kriznih procesa. Predviđanje pomoću umjetne inteligencije ili obuku u virtualnoj stvarnosti navedite kao budući rad samo ako predstavljaju smislen sljedeći korak, a ne kao pretpostavljene funkcionalnosti prve inačice.

Tvrdnja poput „modularna arhitektura omogućuje brzo postavljanje u novim regijama” zahtijeva stvarno projektno uporište. Ovdje nemojte obećavati prilagodljivost samo zato što zvuči kao poželjna korist projekta.

Ovaj pregled zadržite na razini opsega: navedite glavnu mogućnost i njezinu granicu bez popisivanja svakog zahtjeva ili projektne pojedinosti. Ono što je stvarno dovršeno i ono što je ostalo nedovršeno navedite u završnim rezultatima, a ne u ovom početnom opisu.

</details>

## 1.4 Postojeći pristupi i opravdanost projekta

**Cilj:** Objasniti kako korisnici trenutačno rješavaju problem i koja preostala potreba opravdava odobreni projekt.

Organizacija znanstvenih konferencija često se oslanja na fragmentirane postupke i odvojene alate koji omogućuju tek parcijalno zaprimanje radova i komunikaciju. Upravo ta rascjepkanost i potreba za centraliziranim upravljanjem motiviraju razvoj KonfTracka kao jedinstvene platforme koja na jednom mjestu povezuje korisnike, radove, recenzije i odluke. Time se organizacijskim odborima osigurava sustavna podrška za praćenje rokova i očuvanje stroge povjerljivosti postupka, bez preuzimanja uloge samog donošenja odluka.

<details>
<summary><strong>Postojeći pristupi i opravdanost projekta</strong></summary>

**Primjer — CrisisMap:** „Nakon teškog vremenskog događaja građanin će možda morati provjeriti izvor meteoroloških upozorenja i zaseban izvor lokalnih prijava. Predloženi prikaz na karti u CrisisMapu objedinjuje prijave kriznih događaja relevantne za odabranu lokaciju. Aplikacija ne zamjenjuje službena upozorenja ni hitne službe.” Time se objašnjava potreba i namjeravana granica projekta bez tvrdnje da su svi postojeći kanali neučinkoviti. Prva je rečenica **primjer korisničkog scenarija**, a ne izmjeren nalaz o stvarnim korisnicima. Ako tim navodi konkretnu službu upozoravanja ili konkurentski proizvod, treba navesti izvor. Pregled konkurencije i snimke zaslona nisu obavezni.

Ako je postojeće rješenje stvarno utjecalo na projekt, usporedite samo relevantnu funkcionalnost, primjerice jasnoću karte ili potrebnu integraciju. Izbjegavajte unaprijed zadani broj proizvoda ili tablicu kriterija koji nisu povezani s odobrenim zadatkom.

</details>

---

>**Završna provjera:** Opis problema, cilj projekta, korisnici i dionici, granice opsega te postojeći pristupi međusobno su usklađeni. Navedene koristi ne predstavljaju neprovjerene tvrdnje, a uključene i izostavljene funkcionalnosti odgovaraju odobrenom projektnom zadatku.
