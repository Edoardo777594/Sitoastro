# Sito del Dipartimento di Astrofisica

Sito statico (HTML/CSS/JS puro, nessuna build necessaria).

## Struttura

```
index.html        pagina unica del sito
css/style.css      stili
js/main.js         sfondo stellato animato + menu mobile
```

## Come personalizzarlo

Prima di pubblicarlo, sostituisci i contenuti segnaposto in `index.html`:

- nome dell'ateneo e del dipartimento (compare in `<title>`, nell'header e nel footer)
- gruppi di ricerca, coordinatori e descrizioni (sezione `#ricerca`)
- numeri del dipartimento (sezione `#numeri`)
- persone e ruoli (sezione `#persone`)
- pubblicazioni (sezione `#pubblicazioni`)
- seminari e date (sezione `#seminari`)
- indirizzo, email e telefono (sezione `#contatti`)

I colori e i font si modificano in un unico punto: le variabili in cima a `css/style.css` (blocco `:root`).

## Come pubblicarlo su GitHub Pages

1. Crea un nuovo repository su GitHub (es. `dipartimento-astrofisica`).
2. Carica questi tre elementi (`index.html`, la cartella `css/`, la cartella `js/`) nella radice del repository — tramite `git push` oppure trascinandoli nell'interfaccia web di GitHub ("Add file → Upload files").
3. Nel repository vai su **Settings → Pages**.
4. In "Build and deployment", sotto "Source", scegli **Deploy from a branch**.
5. Seleziona il branch `main` e la cartella `/ (root)`, poi salva.
6. Dopo un paio di minuti il sito sarà online all'indirizzo:
   `https://<tuo-utente>.github.io/<nome-repository>/`

Se vuoi che sia raggiungibile su un dominio proprio (es. `astrofisica.tuosito.it`), aggiungi un file `CNAME` nella radice del repository con quel dominio scritto dentro, e configura un record DNS CNAME verso `<tuo-utente>.github.io`.

## Note tecniche

- Non servono framework né passaggi di build: sono file statici.
- I font vengono caricati da Google Fonts via CDN; se preferisci un sito completamente offline-first, puoi scaricarli e servirli localmente.
- Il sito rispetta `prefers-reduced-motion`: chi ha disattivato le animazioni di sistema vedrà lo sfondo stellato statico.
