Funkcijski zahtjevi:

Korisnici i prava pristupa:
	-Registracija korisnika i unos podataka
	-Sigurna prijava (autentifikacija)
	-Sigurna odjava i uništavanje sesije
	-Generiranje i provjera sesija
	-Hashiranje i sigurno spremanje lozinki
	-Promjena lozinke prijavljenog korisnika
	-Zahtjev i postupak za resetiranje lozinke
	-Pregled i uređivanje osobnog profila
	-Definiranje sistemskih uloga (admin, predsjednik, recenzent, autor)
	-Dodjela uloga korisniku po pojedinoj konferenciji
	-Backend provjera prava pristupa


Upravljanje konferencijama:
	-Izrada nove konferencije
	-Pregled popisa dostupnih konferencija
	-Dohvat detaljnih informacija o konferenciji
	-Ažuriranje podataka i opisa konferencije
	-Promjena statusa konferencije (u pripremi, otvorena, zatvorena)
	-Postavljanje roka za predaju radova
	-Postavljanje roka za izradu recenzija
	-Postavljanje roka za donošenje odluka
	-Dodavanje i uređivanje znanstvenih tema konferencije
	-Objavljivanje konferencije (postavljanje vidljivosti)
	-Automatska blokada predaje radova nakon isteka roka
	-Dodjela i provjera prava organizatora nad konferencijom


Sigurnost, validacija i tehnička kvaliteta:
	-Sanitizacija i validacija svih ulaznih podataka iz zahtjeva
	-Zaštita lozinki pomoću jakih algoritmima 
	-Sigurna provjera prava preuzimanja privatnih PDF datoteka
	-Zaštita od curenja osobnih podataka 
	-Centralizirano bilježenje tehničkih pogrešaka 
	-Pisanje unit i integracijskih testova za ključne rute

Predaja znanstvenih radova
	Unos metapodataka rada (naslov, sažetak, ključne riječi)
	Povezivanje rada s odabranom konferencijom i temom
	Unos i povezivanje svih suautora s radom
	Upload PDF datoteke rada
	Provjera dopuštenog formata datoteke (PDF)
	Provjera veličine prenesene datoteke
	Spremanje datoteke na poslužitelj ili pohranu
	Slanje novih verzija rada (ako pravila dopuštaju)
	Praćenje statusa rada (predan, u recenziji, prihvaćen, odbijen)
	Dohvat popisa vlastitih predanih radova za autora
	Uređivanje predanog rada prije isteka roka
	Povlačenje rada od strane autora
	Generiranje i slanje potvrde o uspješnoj predaji

Program konferencije
	Kreiranje sekcija i dvorana/prostorija
	Definiranje satnice i trajanja pojedinih sesija
	Dodjeljivanje prihvaćenih radova u sesije
	Postavljanje prezentera za svaki prihvaćeni rad
	Algoritamska provjera vremenskih preklapanja sesija
	API ruta za javni dohvat objavljenog rasporeda
	Izmjena i ažuriranje rasporeda programa

Statistika i izvještaji
	Agregacija ukupnog broja radova po konferenciji
	Brojanje radova po trenutnim statusima
	Izračun postotka dovršenih i zakašnjelih recenzija
	Sumarno brojanje prihvaćenih i odbijenih radova
	Generiranje i izvoz izvještaja u CSV formatu


Mia:
	- Dvostruko slijepa recenzija (Double-Blind)
	Bilježenje područja stručnosti i interesa recenzenta
	Ručna dodjela recenzenta pojedinom radu
	Automatska detekcija i blokada sukoba interesa
	Prikaz popisa radova dodijeljenih pojedinom recenzentu
	Uklanjanje imena i metapodataka autora iz odgovora recenzentu
	Uklanjanje autorskih podataka iz PDF datoteke (ili provjera anonimnosti)
	Prihvaćanje ili odbijanje zadatka recenziranja
	Pohrana nacrta recenzije (spremak bez konačne predaje)
	Unos ocjena po definiranim kriterijima
	Unos tekstualnih komentara za odbor i za autora
	Zaključavanje i konačna predaja recenzije
	Praćenje rokova i detekcija zakašnjelih recenzija
	Omogućavanje dodjele više recenzenata na isti rad
	Prikaz svih recenzija rada ovlaštenim članovima odbora

	- Odluke o radovima
	Pregled svih pristiglih recenzija za članove odbora
	Unos konačne odluke (prihvaćen, odbijen, potrebna revizija)
	Spremanje vremena i osobe koja je donijela odluku
	Automatska promjena konačnog statusa rada
	Slanje službene obavijesti autoru o odluci
	Dohvat i pregled povijesti svih donesenih odluka

	- Komunikacija i obavijesti
	Slanje e-mail obavijesti o primljenom radu
	Slanje e-mail obavijesti recenzentu o novoj dodjeli
	Slanje e-mail obavijesti autoru o rezultatu recenzije
	Automatizirani pozadinski zadaci (Cron) za slanje podsjetnika
	Korištenje i popunjavanje predložaka e-mail poruka
	Pohrana dnevnika (loga) poslanih i neuspjelih obavijesti

	- Zbornik radova i vanjske integracije (opcionalno)
	Skupljanje svih prihvaćenih radova u zbornik
	Generiranje metapodataka zbornika (naslovi, autori, kazalo)
	Integracija s Crossref API-jem za dohvat/provjeru DOI podatak
	Izvoz rasporeda i programa u vanjske formate (npr. iCal)
	Integracija s ORCID API-jem za verifikaciju identiteta
