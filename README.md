# Naziv projekta
MyCoolinaryBook

## Projektni tim

Ime i prezime | E-mail adresa (FOI) | JMBAG | Github korisničko ime
------------  | ------------------- | ----- | ---------------------
Gabriel Ukić | gukic20@foi.hr | 0023141194 | gukic20


## Opis domene
Projektna domena je upravljanje receptima uz elemente igre za poticanje korisnika na redovito objavljivanje i korištenje same aplikacije. Aplikacije omogućuje korisniku da unosi vlastite recepte, sortira ih po kategorijama uz procijenjenu vremensku pripremu te pretraživanje zapisa prema različitim kriterijima. Svaki recept sastoji se od općih podataka: naziv, autor, kategorija, vrijeme pripreme uz popis sastojaka te količine i mjernih jedinica za iste.
Aplikacija se sastoji od elementa igre: korisnik će skupljati značke ovisno o njegovoj aktivnosti u aplikaciji koje će se temeljiti na njegovoj aktivnosti (npr. prva objava recepta, sedam dana zaredom postavljanje recepata, deset recepata u kategoriji "vegetarijanska jela", jelo za koje potrebno više od pet sati) kako bi se potakla veća aktivnost kod korištenja aplikacije te potakla motivacija za razvijanje kuhinjskih sposobnosti i eksperimentiranja s novim receptima. Domena također obuhvača i autentifikaciju korisnika uz dodatnu mogućnost izvoza recepata u PDF format za jednostavno dijeljenje izvan aplikacije.

## Specifikacija projekta

Oznaka | Naziv | Kratki opis 
------ | ----- | ----------- 
F01 | Autentifikacija | Za pristup aplikaciji potrebna je autentifikacija korisnika (registracija prije prve prijave u sustav te prijava) putem Firebase Authentication servisa. Korisnik će se registrirati u aplikaciju nakon pravilnog popunjavanja forme, a kod prijave unositi će email i lozinku. 
F02 | Upravljanje receptima | Svaki recept sadrži: naziv, kategoriju, opis, tip jela, vrijeme pripreme, vrijeme kuhanja, popis sastojaka (s količinom i mjernim jedinicama), datum kreiranja te procjenu broja kalorija. Korisnik će imati mogućnost filtriranje svoje liste recepata po: nazivu, kategoriju, datumu i vremenu pripreme.
F03 | Dodjela badgeva | Aplikacija će pratiti korisničku aktivnost te na temelju iste, prema definiranim pravilima, dodijeljivati značke. Korisnik će moći pregledati svoje osvojene značke, kao i ostale moguće značke koje mu nisu dodijeljene. Značke će se dodijeljivati na temelju: broja kreiranih recepata, broj recepata u pojedinoj kategoriji, uzastopnim danima kreiranosti i slično.
F04 | Izvoz recepata u PDF | Korisnik može izvesti svoje odabrane recepte u PDF dokument te će mu biti moguće spremiti isti na uređaj ili podijeliti preko drugih aplikacija. Dokument će sadržavati osnovne podatke o receptu i popis sastojaka uz pripadajuću fotografiju

## Arhitektura
Aplikacija je organizirana prema Model-View-ViewModel obrascu koji je podijeljen u tri sloja:
- data - Room entiteti, DAO sučelja i implementacija repozitorija
- domain - use case-ovi za validaciju i poslovnu logiku uz domenske modele
- ui - Ekrani, ViewModeli i navigacijska struktura aplikacije

Podaci se pohranjuju lokalno u Room bazi podataka, dok se autentifikacija korisnika pbavlja preko Firebase Authentication servisa.


## Tehnologije i oprema
MyCoolinaryBook je mobilna aplikacija za Android uređaje koja kombinira standardne funkcionalnosti s elementima igara. Za razvoj se koriste:
- Android Studio – razvojno okruženje za izradu Android aplikacije.
- Kotlin – programski jezik korišten za implementaciju aplikacije.
- Room Database – lokalna baza podataka za spremanje recepata, sastojaka, badgeva i komentara.
- Firebase Authentication – autentifikacija korisnika putem emaila i lozinke.
- Kotlin Coroutines&Flow – asinkrono izvođenje operacija i upravljanje podacima.
- MVVM arhitektura – organizacija aplikacije kroz data, domain i presentation slojeve.
- Git – verzioniranje izvornog koda.
- GitHub – pohrana izvornog koda i suradnja na projektu.
- Jira – planiranje sprintova, backloga i praćenje razvoja projekta.
- Confluence – projektna dokumentacija, sprint planovi i Definition of Done.

Za razvoj projekta koristi se razvojno stolno/prijenosno računalo s instaliranim Android Studiom, potrebnim Android SDK komponentama te pristupom Firebase konzoli za konfiguraciju autentifikacije.
