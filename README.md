
## DRUGI KOLOKVIJ

<details>
<summary><strong>1. Što je SQL i navedite njegove osobine?</strong></summary>

**SQL** (Structured Query Language) je strukturirani jezik za pretraživanje i njegove osobine su:

1. English-like jezik. Upotrebljava riječi kao što su npr.: select, insert, delete i sl. kao dio naredbe
   
2. Ne-proceduralni jezik
   
3. U jednom trenutku češće obrađuje skup slogova nego jedan slog (na razini tablice)
   
4. Mogu ga koristiti korisnici različitog profila: DB administratori, aplikativni programeri, neprofesionalni korisnici i sl.
   
5. Osigurava naredbe za različite zadaće uključujući:
   - Upite nad podacima  Dodavanje, mijenjanje i brisanje redaka u tablicama
   - Kreiranje, mijenjanje i brisanje objekata sheme
   - Kontrolu pristupa bazi podataka i objektima sheme
   - Osigurava konzistentnost baze podataka
  
</details> 

---
<br>
<br> 

<details>
<summary><strong>2. Navedite i opišite objekte SQL-a.</strong></summary>

**Baza podataka (Database)** - najviša razina organizacije (spremnik za sve ostale objekte).

**Tablica (Table) ** - fizički pohranjuje podatke u retke i stupce.

**Pogled ili virtualna tablica (View)** - spremljeni SELECT upit koji se ponaša kao tablica, ali ne pohranjuje podatke.

**Pravilo integriteta (Constraint)** - ograničenja koja osiguravaju ispravnost i konzistentnost podataka.

**Indeks (Index)** - struktura za ubrzavanje pretraživanja kao kazalo u knjizi.

**Procedura (Stored Procedure)** - spremljeni skup SQL naredbi koji se može pozivati po imenu, poput funkcije.

**Okidač (Trigger)** - automatski se izvršava kada se dogodi određena akcija na tablici

**Sinonim (Synonym)** - alternativno ime za drugi objekt baze podataka.

</details> 

---
<br>
<br> 

<details>
<summary><strong>3. Navedite tipove podataka u SQL-u.</strong></summary>

1. INTEGER
2. SMALLINT
3. TINYINT
4. CHAR
5. NCHAR
6. VARCHAR
7. TEXT
8. DECIMAL
9. DATETIME
  - SMALLDATETIME
  - TIMESTAMP 
10. BINARY
11. VARBINARY
12. IMAGE
    
</details> 

---
<br>
<br> 

<details>
<summary><strong>4. Navedite tipove SQL izraza (funkcija).</strong></summary>

1. DML izrazi (Data Manipulation Language Statements) tj. izrazi za upravljanje podacima 
2. DDL izrazi (Data Definition Language Statements) tj. izrazi za definiranje podataka
3. Izrazi za kontrolu transakcija (Transaction Control Statements)
4. Izrazi za kontrolu sesije (Session Control Statements)
5. Izrazi za kontrolu sustava (System Control Statements)
6. Ugrađeni SQL izrazi (Embedded SQL Statements)

</details> 

---
<br>
<br> 

<details>
<summary><strong>5. Navedite osnovne metode spajanja.</strong></summary>
   
1. EQUI-JOIN 
2. NON-EQUI JOIN
3. OUTER JOINS
4. SELF JOINS

</details> 

---
<br>
<br> 

<details>
<summary><strong>6. Što su podupiti i navedite primjer?</strong></summary>

**Podupit** je SELECT iskaz ugnježđen u drugom SELECT iskazu.
  SELECT ImePrezime, RadnoMjesto, plaća 
  FROM djelatnici 
  WHERE plaća=(SELECT MIN(plaća) 
    FROM djelatnici);

</details> 

---
<br>
<br> 

<details>
<summary><strong>7. Što su pogledi i zašto se koriste?</strong></summary>

**Pogledi** su virtualne tablice koje se dobivaju izvršavanjem SQL upita nad jednim ili više stvarnih tablica.

Koriste se za:
1. pojednostavljenje složenih upita
2. ograničavanje pristupa podacima (sigurnost)
3. prikaz samo određenih podataka (filtriranje)
4. povezivanje više tablica u jedan prikaz

</details> 

---
<br>
<br> 

<details>
<summary><strong>8. U čemu je razlika između pogleda i relacije (tablice)?</strong></summary>

**TABLICE** – fizička pohrana podataka na disk te oni postoje neovisno  o upitima, zauzima memorisjki prostor, podaci se mijenjaju pomoću naredba INSERT, UPDATE, DELETE
**POGLEDI** – pohranjuju samo definiciju upita, svaki put kada se pozove, izvršava upit iznova, podaci dolaze iz osnovnih tablica, zauzima gotovo nikakav prostor

</details> 

---
<br>
<br> 

<details>
<summary><strong>9. Što su funkcije i kad se koriste?</strong></summary>

**Funkcija** je potprogram koji u pozivajući program vraća rezultat kao povratnu vrijednost

Koriste se:
▪	Kada isti izračun koristiš na više mjesta  
▪	Kada želiš pojednostaviti složene upite 
▪	Kada trebaš transformirati ili formatirati podatke 
▪	Kada želiš enkapsulirati poslovnu logiku 
▪	Kada trebaš vrijednost direktno u SELECT upitu

</details> 

---
<br>
<br> 

<details>
<summary><strong>10. Što su procedure i kad se koriste?</strong></summary>

**Procedura** je potprogram koji u pozivajući program ne vraća rezultat kao povratnu vrijednost

Koriste se:
▪	Kada trebaš izvršiti složenu poslovnu logiku  
▪	Kada iste operacije ponavljaš više puta  
▪	Kada radiš s transakcijama (više povezanih operacija)  
▪	Kada želiš povećati sigurnost (korisnici ne vide tablice, samo pozivaju proceduru) 
▪	Kada trebaš INSERT, UPDATE ili DELETE operacije

</details>

---
<br>
<br> 

<details>
<summary><strong>11. Što su okidači i kad se koriste?</strong></summary>

**Okidač** je programski kod koji se izvršava automatski prilikom izvođenja specificirane DML operacije nad specificiranom tablicom

Koriste se za:
▪	Logiranje (automatsko bilježenje svih promjena u bazi)
▪	Validaciju (provjera ispravnosti podataka pri unosu)  
▪	Reviziju(Audit) (praćenje tko je i kada mijenjao podatke)  
▪	Automatsko ažuriranje (održavanje izvedenih podataka)  
▪	Sigurnost (sprječavanje neovlaštenog brisanja podataka) 

</details> 

---
<br>
<br> 

<details>
<summary><strong>12. Što je ECA?</strong></summary>

**ECA** odnosno, **Event–Condition–Action** (Događaj–Uvjet–Akcija) je princip koji se koristi u bazama podataka (npr. kod triggera):

**Event (događaj)** – nešto se dogodi (npr. INSERT, UPDATE, DELETE)
**Condition (uvjet)** – provjerava se određeni uvjet
**Action (akcija)** – ako je uvjet ispunjen, izvršava se neka radnja

</details>

---
<br>
<br> 

<details>
<summary><strong>13. Što je integritet baze podataka i navedite integritetska ograničenja?</strong></summary>

**Integritet baze** podataka se odnosi na ispravnost podataka koji se u njoj nalaze

Entitetski integritet (eng. Entity integrity)
Domenski integritet (eng. Domain integrity) 
Ograničenja NULL vrijednosti (eng. Constraints on NULL) 
Integritet ključa (eng. Key integrity) 
Referencijalni integritet (eng. Referential integrity) 
Opća integritetska ograničenja (eng. General integrity constraints)

</details> 

---
<br>
<br> 

<details>
<summary><strong>14. Što je sigurnost baze podataka i kako može biti narušena?</strong></summary>

**Sigurnost baze podataka** (eng. database security) brine se o tome da korisnici koji pristupaju bazi podataka za to imaju ovlaštenje

Može biti narušena na više načina: 

Korisnik neovlašteno čita podatake
Korisnik neovlašteno mijenja podatake 
Korisnik neovlašteno briše podatake

</details> 

---
<br>
<br> 

<details>
<summary><strong>15. Što je fizička organizacija baze podataka?</strong></summary>

Pod pojmom fizičke organizacije baze podataka podrazumijevamo strukture podataka korištene pri spremanju podataka u memoriji 
Fizička organizacija baze podataka ne utječe na rezultate operacija s podacima 
Utječe na učinkovitost baze podataka jer djelotvornija fizička organizacija brže pristupa podacima

</details> 

---
<br>
<br> 

<details>
<summary><strong>16. Koje su najčešće metode fizičke organizacije baze podataka?</strong></summary>

1. Neporedana datoteka (eng. heap) 
2. Poredana datoteka (eng. sorted file) 
3. Raspršena datoteka (eng. hash file)  Indeksno-slijedna organizacija (eng. index-sequential file) 
4. B-stablo (eng. B-tree)

</details> 

---
<br>
<br> 

<details>
<summary><strong>17. Objasnite B-stablo.</strong></summary>

**B-stablo** je balansirano stablo koje se koristi za brzo pretraživanje podataka u bazi.

- Balansirano znači da je put od korijena do svakog lista jednak, pa je pristup podacima uvijek učinkovit
- Pretraga počinje od korijena
- U svakom čvoru se bira odgovarajući pokazivač prema vrijednosti ključa
- Postupak se ponavlja dok se ne dođe do lista gdje se nalazi traženi podatak

</details>

---
<br>
<br> 

<details>
<summary><strong>18. Što su indeksi?</strong></summary>


**Indeksi** u bazi podataka su pomoćne strukture koje se koriste za brže pretraživanje podataka.

Kreiraju se nad jednim ili više atributa (stupaca), najčešće su organizirani kao B-stablo i sadrže vrijednosti ključa i pokazivače na stvarne zapise

Svrha im je ubrzavanje dohvata podataka i izbjegavanje sporog linearnog pretraživanja svih zapisa

</details>

---
<br>
<br> 

<details>
<summary><strong>19. Nabrojite i pojasnite tzv. ACID osobine transakcija.</strong></summary>

**Atomiziranost (engl. atomicity)** – ‘sve ili ništa’, predstavlja nedjeljivost transakcije. Transakcija se mora obaviti čitava ili ništa
**Konzistentnost (engl. consistency)** – transakcija mora transformirati bazu iz jednog konzistentnog stanja u drugo. 
**Izoliranost (engl. isolation)** – transakcije se izvršavaju neovisno jedna od druge i djelovanje mora biti isto kao da se obavljaju jedna iza druge 
**Trajnost (engl. durability)** – rezultat uspješno završenih (potvrđenih) transakcija se trajno bilježi u bazu podataka i ne smije se izgubiti zbog eventualnih naknadnih grešaka.

</details> 

---
<br>
<br> 

<details>
<summary><strong>20. Ako je podatak zaključan ekskluzivnim (exclusive ili write) ključem, koje zaključavanje može dobiti sljedeća transkacija koja traži pristup istom podatku?</strong></summary>


Ekskluzivno zaključavanje blokira sve ostale pristupe tako nijedna druga transakcija ne može dobiti nikakvo zaključavanje, mora čekati dok se ekskluzivni zaključak ne oslobodi.

</details> 

---
<br>
<br> 

<details>
<summary><strong>21. Što je distribuirana baza podataka?</strong></summary>

**Distribuirana baza podataka** je skup baza podataka smještenih na više različitih računala i prostornih lokaliteta, a s kojima korisnik radi kao da je u pitanju jedna jedinstvena baza.

</details> 

---
<br>
<br> 

<details>
<summary><strong>22. Pojasnite način funkcioniranja protokola dvofaznog potvrđivanja transakcija kod distribuiranih baza podataka!</strong></summary>


1. Glavni čvor šalje poruku o ažuriranju potčinjenim čvorovima: “napravi brzu potvrdu prijema” 
2. Potčinjeni čvor odgovara s “potvrđujem prijem” 
3. Glavni šalje poruku “potvrdi bazu podataka”
4. Potčinjeni odgovara s “potvrđeno”.

</details> 

---
<br>
<br> 

<details>
<summary><strong>23. Značajke DDBMS-a.</strong></summary>

1. Skup logički povezanih djeljivih podataka 
2. Podaci su razdvojeni na više fragmenata 
3. Fragmenti se mogu replicirati 
4. Fragmenti/Replikacije pripadaju lokacijama 
5. Lokacije su povezane komunikacijskom mrežom
6. Podaci na svakoj lokaciji su pod nadzorom DBMS-a 
7. DBMS na svakoj lokaciji može upravljati lokalnim aplikacijama autonomno 
8. Svaki DBMS učestvuje u najmanje jednoj globalnoj aplikaciji.

</details> 

---
<br>
<br> 

<details>
<summary><strong>24. Navedite 4 osnovna dijela DDBMS-a.</strong></summary>

1. Lokalna DBMS komponenta 
2. Komunikacijska komponenta
3. Globalni katalog sustava
4. Distribuirana DBMS komponenta
   
</details>

---
<br>
<br> 

<details>
<summary><strong>25. Navedite 4 osnovne strategije alociranja.</strong></summary>

1. Centralizirana
2. Fragmentirana
3. Potpuna replikacija
4. Selektivna replikacija

</details>

---
<br>
<br> 

<details>
<summary><strong>26. Što su NoSQL baze podataka i navedite najčešće?</strong></summary>

**NoSQL baze** ne-relacijske baze podataka novije generacije, većinom su otvorenog koda, horizontalno skalabilne, jednostavan API, BASE (nisu ACID), rade s velikom količinom podataka itd.

Najčešće:
1. Dokumenti 
2. Ključ-vrijednost
3. Grafovi
4. Objektne orijentirane baze podataka
   
</details> 

---
<br>
<br> 

<details>
<summary><strong>27. Što je skladište podataka?</strong></summary>


**Skladište podataka** je predmetno orijentirani, integrirani, relativno stabilni i vremenski orijentirani skup podataka u funkciji potpore odlučivanja menadžera.

</details> 
---
<br>
<br> 

<details>
<summary><strong>28. Zašto su metapodaci posebno značajni kod skladišta podataka?</strong></summary>


Jer opisuju izvore podataka, strukturu i značenje podataka, sadrže informacije o procesima (ETL), transformacijama i prijenosu podataka, omogućuju integraciju, uniformnost i konzistentnost podataka te pomažu korisnicima da razumiju i pravilno koriste podatke

</details> 

---
<br>
<br> 

<details>
<summary><strong>29. U čemu je temeljna razlika između baza podataka i skladišta podataka?</strong></summary>


**Baze podataka (operativne)** služe za svakodnevne transakcije (unos, izmjena, brisanje), podaci su detaljni i često se mijenjaju dok **skladišta podataka (data warehouse)** služe za analizu i donošenje odluka podaci su integrirani, povijesni i uglavnom se ne mijenjaju

</details>

---
<br>
<br> 

<details>
<summary><strong>30. Koji je najčešći model podataka u skladišu podataka i navedite osnovna svojstva?</strong></summary>


Najčešći model je **Dimenzijski model**, a njegova osnovna svojstva su:

- Jedna “glavna” tablice sa složenim ključem nazvane vrijednosna tablica, skup manjih tablica nazvanih dimenzijske tablice.

- Svaka dimenzijska tablica ima jedinstveni primarni ključ koji odgovara točno jednom dijelu složenog ključa u vrijednosnoj tablici. To stvara strukturu sličnu zvijezdi, pa se ovaj model često naziva i zvijezda spajanje.

</details> 

---
<br>
<br> 

<details>
<summary><strong>31. Opišite logičku i fizičku strukturu baze podataka.</strong></summary>

**Logička** opisuje kako su podaci organizirani s korisničkog pogleda:

- Tabelarni prostor (eng. tablespace)
- Objekt sheme (eng. schema object) -
- Segment (eng. segment)
- Mjera (eng. extent)
- Blok podataka (eng. data block)

Fizička opisuje kako su podaci stvarno pohranjeni na disku:

- Datoteka podataka (eng. data file)
- Datoteka za obnavljanje (eng. redo log file)
- Kontrolna datoteka (eng. control file)
  
</details> 

---
<br>
<br>
