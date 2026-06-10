# FAQ

## 1. Il sito funziona senza internet?

In parte sì. Le pagine HTML, il CSS, il file `data.json` e l'immagine locale sono nel progetto. Bootstrap però arriva da CDN, quindi per vedere lo stile completo serve internet. Senza connessione il sito resta leggibile. Meno rifinito, ma leggibile.

## 2. Perché i dati non compaiono?

Quasi sempre succede perché il sito è stato aperto con doppio click su `index.html` o `rischi.html`. Il file `script.js` usa `fetch("data.json")`, quindi serve un server locale. Avvia `python -m http.server 8000` e apri `http://localhost:8000`. Piccola mossa, grande svolta!

## 3. Come modifico i contenuti delle schede?

Devi modificare il file `data.json`. Ogni elemento contiene titolo, categoria, descrizione e campi come rischio, consiglio e target. Attenzione alle virgole: nel JSON una virgola messa male può bloccare tutto, e nessuno vuole litigare con una virgola!

## 4. A cosa serve `script.js`?

`script.js` legge i dati da `data.json`, crea le card, popola il filtro categorie, aggiorna il numero di risultati e costruisce la tabella. In pratica è il motore della pagina `rischi.html`.

## 5. Dove trovo la checklist?

La checklist si trova in `buone-pratiche.html`. È pensata come una lista rapida di azioni concrete: password diverse, backup, aggiornamenti, attenzione ai link e un po' di sano dubbio quando qualcosa online sembra troppo comodo.

## 6. Posso aggiungere altri rischi?

Certo! Aggiungi un nuovo oggetto dentro l'array `items` di `data.json`, mantenendo la stessa struttura degli altri elementi. Se rispetti i campi già usati, lo script lo mostrerà automaticamente.
