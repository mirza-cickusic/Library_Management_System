# Jednostavni sistem za upravljanje bibliotekom

Studentski projekat napisan u Javi. Program omogućava osnovnu evidenciju knjiga, članova i posudbi, a podatke čuva u običnim tekstualnim fajlovima.

## Funkcionalnosti

- Dodavanje i prikaz knjiga.
- Pretraga knjiga po naslovu ili autoru.
- Registracija i prikaz članova.
- Posudba i povrat knjige.
- Pregled aktivnih posudbi i datuma vraćanja.
- Ograničenje od tri aktivne posudbe po članu.
- Rok posudbe od 14 dana.
- Automatsko čuvanje podataka u TXT fajlovima.

## Tehnologije

- Java 11 ili novija.
- Standardna Java biblioteka.
- Nema SQL baze, JDBC-a, Maven-a ni dodatnih biblioteka.

## Pokretanje u IntelliJ IDEA

1. Klonirajte repozitorij ili preuzmite projekat.
2. Otvorite projekat u IntelliJ IDEA.
3. Provjerite da je izabran JDK 11 ili noviji.
4. Otvorite `Main.java`.
5. Pokrenite metodu `main` klikom na zelenu strelicu pored nje.

Sve Java klase nalaze se u jednom fajlu `Main.java`, tako da nije potrebno posebno dodavati druge `.java` fajlove.

## Čuvanje podataka

Prilikom prvog pokretanja program automatski napravi mapu `data` i tri fajla:

```text
data/
├── books.txt
├── members.txt
└── loans.txt
```

Svaki red predstavlja jedan zapis. Polja su razdvojena znakom `|`:

- `books.txt`: `id|naslov|autor|isbn`
- `members.txt`: `id|ime i prezime|e-mail`
- `loans.txt`: `id|idKnjige|idClana|datumPosudbe|rokVracanja|vraceno`

Nemojte brisati mapu `data` ako želite sačuvati podatke. Znak `|` nije dozvoljen u unosima jer se koristi kao razdvajač polja.

## Primjer korištenja

1. Izaberite **Dodaj knjigu** i unesite naslov, autora i ISBN.
2. Izaberite **Registruj člana**.
3. Prikažite knjige i članove da vidite njihove ID-jeve.
4. Izaberite **Posudi knjigu** i unesite ID knjige i ID člana.
5. Pregledajte aktivne posudbe, pa unesite ID posudbe u opciji **Vrati knjigu**.

## Ograničenja projekta

Napomena: Ovo je namjerno jednostavna akademska verzija. Svaki naslov predstavlja jedan primjerak. Program nema korisničke naloge, grafički interfejs, rezervacije, kazne, više primjeraka istog naslova ni mrežnu bazu podataka.
