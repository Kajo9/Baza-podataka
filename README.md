# Baza-podataka
## FOI projekt kolegij Baze podataka
# Analiza pjesama na platformi Spotify

Projekt izrađen u sklopu kolegija **Modeliranje i primjena skladišta podataka** na Fakultetu organizacije i informatike (FOI), Sveučilišta u Zagrebu.

Cilj projekta bio je analizirati podatke o pjesmama na platformi Spotify, transformirati izvorni skup podataka u strukturirano skladište podataka te izraditi vizualizacije koje omogućuju pregled različitih glazbenih karakteristika, popularnosti pjesama, žanrova, izvođača i albuma.

## Korištene tehnologije

- **Microsoft Excel** – Početni pregled, priprema i uređivanje podataka.
- **Microsoft Access** – Upravljanje podacima, SQL upiti, ETL transformacije i implementacija skladišta podataka.
- **Tableau** – Vizualizacija podataka, izrada izvještaja i analitičkih prikaza.

## Skup podataka

Za analizu je korišten skup podataka *Top 10000 Songs on Spotify 1960–Now*, preuzet s platforme Kaggle.

Skup podataka sadrži informacije o pjesmama na Spotifyju, uključujući:

- Nazive pjesama i izvođača
- Informacije o albumima i datumima izdanja
- Glazbene žanrove i podžanrove
- Popularnost pjesama
- Plesnost (*danceability*) i energiju (*energy*)
- Akustičnost (*acousticness*) i instrumentalnost (*instrumentalness*)
- Glasnoću (*loudness*), tempo i trajanje pjesama
- Ostale audio karakteristike

**Izvor podataka:** [Top 10000 Songs on Spotify 1960–Now – Kaggle](https://www.kaggle.com/datasets/joebeachcapital/top-10000-spotify-songs-1960-now/data)

## Tijek projekta

### 1. Ekstrakcija podataka

- Uvoz izvornog CSV skupa podataka u Microsoft Excel.
- Pregled i početna priprema podataka.
- Uvoz pripremljenih podataka u Microsoft Access.

### 2. Transformacija podataka

- Čišćenje i reorganizacija uvezenih podataka.
- Prilagodba tipova podataka i formata datuma.
- Preimenovanje stupaca radi bolje preglednosti.
- Korištenje SQL upita u Microsoft Accessu za transformaciju i pripremu podataka.
- Izrada dimenzijskih tablica i tablice činjenica.

### 3. Skladište podataka – zvjezdasta shema

Implementirano je skladište podataka prema modelu zvjezdaste sheme (*Star Schema*), koje se sastoji od sljedećih tablica:

**Dimenzijske tablice:**

- `Datumi` – Podaci o datumima, uključujući dane, mjesece, tromjesečja i godine.
- `Pjesma` – Nazivi pjesama i informacije o izvođačima.
- `Album` – Informacije o albumima.
- `Playlista` – Nazivi playlista, žanrovi i podžanrovi.

**Tablica činjenica:**

- `Spotify` – Središnja tablica koja sadrži glazbene karakteristike pjesama i poveznice prema dimenzijskim tablicama.

### 4. Vizualizacija i izvještavanje

Skladište podataka povezano je s alatom Tableau, u kojem su izrađeni vizualni izvještaji za analizu različitih aspekata skupa podataka.

Analiza obuhvaća:

- **Popularnost pjesama prema žanru** – Pregled agregirane popularnosti pjesama unutar različitih žanrova.
- **Prosječna energija i tempo** – Usporedba glazbene energije i tempa prema izvođačima, žanrovima i albumima.
- **Popularnost i plesnost pjesama** – Analiza prosječne popularnosti i plesnosti prema albumima i godinama izdanja.
- **Glasnoća prema playlistama** – Pregled maksimalnih vrijednosti glasnoće unutar pojedinih playlista.
- **10 najpopularnijih pjesama** – Izdvajanje najpopularnijih pjesama iz skupa podataka.

## Cilj projekta

Glavni cilj projekta bio je prikazati postupak izrade skladišta podataka primjenom ETL pristupa te korištenje alata za vizualizaciju podataka radi dobivanja korisnih uvida iz velikog skupa glazbenih podataka.

Projekt objedinjuje rad s relacijskim bazama podataka, SQL transformacije, dimenzijsko modeliranje i interaktivno izvještavanje.

## Autor

**Karlo Alković**

Fakultet organizacije i informatike (FOI), Sveučilište u Zagrebu

Kolegij: Modeliranje i primjena skladišta podataka
