# Il Viaggio — pubblicazione su GitHub Pages + installazione PWA su iPhone

## File in questa cartella
- `index.html` — la tua pagina (rinominata da `page.html`, GitHub Pages richiede `index.html`)
- `manifest.json` — configurazione PWA (nome, icone, colori)
- `sw.js` — service worker minimo, permette l'installazione e il funzionamento offline
- `icon-192.png`, `icon-512.png` — icone generate per l'app
- **Devi aggiungere tu**: `foto.jpeg` e `boarding_pass.png` (le tue due immagini originali), nella stessa cartella

## 1. Pubblicare su GitHub Pages

1. Vai su https://github.com e crea un nuovo repository (es. "il-viaggio"), pubblico.
2. Carica in quel repository TUTTI i file di questa cartella, incluse le tue due immagini
   `foto.jpeg` e `boarding_pass.png` (drag & drop dalla pagina web del repo, oppure con git).
3. Nel repository vai su **Settings → Pages**.
4. In "Build and deployment" → Source, scegli **Deploy from a branch**.
5. Branch: **main**, cartella: **/(root)** → Save.
6. Dopo 1-2 minuti il sito sarà live su:
   `https://TUONOMEUTENTE.github.io/il-viaggio/`

## 2. Installare come app sull'iPhone (PWA)

1. Apri il link del sito con **Safari** (importante: deve essere Safari, non Chrome).
2. Tocca l'icona di condivisione (il quadrato con la freccia verso l'alto).
3. Scorri e tocca **"Aggiungi a Home"**.
4. Conferma il nome e tocca "Aggiungi".

L'app apparirà come icona sulla schermata Home, si aprirà a schermo intero
(senza barra Safari) e funzionerà anche offline dopo il primo caricamento.

## Note
- Se in futuro modifichi `index.html`, cambia anche `CACHE_NAME` in `sw.js`
  (es. da `il-viaggio-v1` a `il-viaggio-v2`) altrimenti iOS potrebbe continuare
  a mostrare la versione vecchia salvata in cache.
- Tutto il sito è statico (HTML/CSS/JS), quindi GitHub Pages è perfetto: nessun
  server o database necessario.
