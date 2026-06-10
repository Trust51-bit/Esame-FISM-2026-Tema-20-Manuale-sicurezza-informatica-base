# API locale

In questo progetto non c'è una vera API online. L'API è simulata dal file:

```text
data.json
```

Comodo, leggero e perfetto per un esercizio: i dati restano nella repository e il sito li legge come se arrivassero da una fonte esterna.

## Quali dati contiene

Il file contiene una sezione `meta` e un array `items`.

La sezione `meta` descrive il progetto e le colonne della tabella. L'array `items` contiene le schede sui rischi di sicurezza informatica.

## Campi usati

Ogni elemento usa questi campi principali:

- `id`: identificativo dell'elemento;
- `title`: nome dell'argomento;
- `subtitle`: breve etichetta della scheda;
- `category`: categoria del rischio;
- `description`: descrizione del problema;
- `fields.rischio`: livello di rischio;
- `fields.consiglio`: suggerimento pratico;
- `fields.utente_target`: tipo di utente interessato;
- `fields.controllo`: controllo o azione consigliata.

## Dove li trovi nel sito

Nella pagina `rischi.html` trovi i dati in due modi:

- come card Bootstrap, utili per leggere ogni rischio con calma;
- come tabella responsive, comoda per confrontare le informazioni in modo rapido.

La ricerca e il filtro categoria lavorano sugli stessi dati. Scrivi una parola, scegli una categoria e la pagina si aggiorna. Niente effetti speciali inutili, solo praticità!

## Come lo script carica il file

Il file `script.js` usa:

```js
fetch("data.json")
```

Poi trasforma la risposta in JSON e usa i dati per generare card, tabella e filtri.

Per questo motivo il sito deve essere aperto con un server locale. Se lo apri con doppio click, il browser può bloccare la lettura del file. Soluzione rapida:

```bash
python -m http.server 8000
```

Poi apri:

```text
http://localhost:8000
```
