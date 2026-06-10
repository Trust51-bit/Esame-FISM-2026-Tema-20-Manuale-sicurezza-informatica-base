# Manuale sicurezza informatica base

Benvenuto nel progetto FISM 2026 - Tema 20! Questo sito è un piccolo manuale web sulla sicurezza informatica di base: parla di password, phishing, backup, Wi-Fi pubblico e altre situazioni che sembrano innocue... finché non combinano guai!

L'obiettivo è semplice: spiegare i rischi digitali con parole chiare e consigli che puoi usare subito. Niente frasi fredde da manuale polveroso. Qui si va dritti al punto.

## Funzionalità principali

- sito multipagina con `index.html`, `rischi.html`, `buone-pratiche.html`, `area-principianti.html` e `area-esperti.html`;
- navbar Bootstrap responsive e collegamenti tra tutte le pagine;
- dati presi dal file locale `data.json`;
- card create automaticamente tramite `script.js`;
- ricerca e filtro per categoria nella pagina dei rischi;
- tabella Bootstrap responsive con i dati principali;
- pagina dedicata alle buone pratiche con checklist concreta;
- area principianti con percorso guidato, consigli pratici e link ufficiali agli strumenti base;
- area esperti con controlli più tecnici e procedure da sviluppatore;
- immagine locale salvata in `assets/immagini/`;
- documentazione nella cartella `docs/`.

## Tecnologie usate

- HTML per la struttura delle pagine;
- CSS per personalizzare colori, spazi e dettagli grafici;
- Bootstrap per navbar, griglia, card, bottoni, badge e tabella;
- JavaScript per leggere `data.json` e mostrare i dati;
- JSON per simulare una piccola API locale.

## Avvio rapido

Questo progetto usa `fetch("data.json")`, quindi non conviene aprire `index.html` con doppio click. Il browser può bloccare i dati e le card spariscono. Fastidioso? Sì. Normale? Anche.

Apri il terminale nella cartella del progetto ed esegui:

```bash
python -m http.server 8000
```

Poi apri il browser su:

```text
http://localhost:8000
```

In alternativa puoi usare Live Server di Visual Studio Code.

## Requisiti

- un browser moderno;
- Python installato, se vuoi usare il comando `python -m http.server 8000`;
- connessione internet per caricare Bootstrap dal CDN;
- un pizzico di attenzione quando modifichi `data.json`, perché una virgola fuori posto può rovinare la festa!

## Struttura del progetto

```text
Esame-FISM-2026-Tema-20-Manuale-sicurezza-informatica-base/
├── README.md
├── index.html
├── rischi.html
├── buone-pratiche.html
├── area-principianti.html
├── area-esperti.html
├── style.css
├── script.js
├── data.json
├── docs/
│   ├── installazione.md
│   ├── faq.md
│   └── api.md
└── assets/
    └── immagini/
        └── sicurezza-informatica-hero.png
```

## Documentazione utile

- [Installazione](docs/installazione.md)
- [FAQ](docs/faq.md)
- [API locale](docs/api.md)

## Nota su `script.js` e `data.json`

I file `script.js` e `data.json` sono quelli forniti come base dell'esercizio. Il sito li usa per mostrare i rischi nella pagina `rischi.html`. Il codice JavaScript legge il JSON, crea le card, aggiorna il conteggio, applica i filtri e costruisce la tabella.

## Autore

Progetto realizzato per l'esame FISM 2026 - Tema 20.

## Licenza

Nel progetto è presente un file `LICENSE`. La licenza serve a chiarire come può essere usato o riutilizzato il materiale della repository. Anche quando un progetto è piccolo, mettere le regole nero su bianco è una buona abitudine: ordine prima di tutto!
