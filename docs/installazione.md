# Installazione

Questa guida spiega come aprire il progetto senza perdere tempo dietro a problemi evitabili. La parola chiave è: server locale!

## 1. Clonare la repository

Apri il terminale e usa:

```bash
git clone URL-DELLA-REPOSITORY
```

Poi entra nella cartella:

```bash
cd Esame-FISM-2026-Tema-20-Manuale-sicurezza-informatica-base
```

## 2. Avviare il server locale

Dentro la cartella del progetto esegui:

```bash
python -m http.server 8000
```

Se il comando parte correttamente, il terminale resta occupato e mostra che il server è in ascolto. Tutto normale: sta facendo il suo lavoro!

## 3. Aprire il sito

Nel browser visita:

```text
http://localhost:8000
```

Da lì puoi navigare tra:

- `index.html`
- `rischi.html`
- `buone-pratiche.html`

## Problema tipico: i dati non compaiono

Se apri il file HTML con doppio click, il browser potrebbe bloccare `fetch("data.json")`. Non è il sito che fa i capricci: è una regola di sicurezza del browser.

Soluzione: avvia il server locale con `python -m http.server 8000` oppure usa Live Server in Visual Studio Code. Una volta aperto da `localhost`, le card e la tabella tornano al loro posto!
