# Simulatore «Tetto al gas e capacità trattenuta»

App web installabile (PWA): funziona da browser, si installa sul telefono e va anche senza connessione.
Tutti i valori sono inventati e servono solo a scopo didattico.

## Cosa c'è nella cartella

- `index.html`: il simulatore completo (installabile come app)
- `breve.html`: la versione compatta, da condividere su LinkedIn
- `anteprima.png`: l'immagine che LinkedIn mostra sotto il link
- `manifest.webmanifest`: nome, icone e colori dell'app installata
- `sw.js`: fa funzionare l'app senza connessione
- `icons/`: icone dell'app
- `fonts/`: caratteri Barlow (licenza libera SIL OFL, in `fonts/OFL.txt`), così l'app non chiama servizi esterni
- `.nojekyll`: file vuoto che serve a GitHub Pages (su alcuni computer è nascosto: non è indispensabile)

## Pubblicarla gratis con GitHub Pages (consigliato da computer)

1. Decomprimi lo zip.
2. Crea un account gratuito su github.com.
3. In alto a destra: **+ › New repository**. Nome, per esempio, `simulatore-tetto-gas`. Lascia **Public** e premi **Create repository**.
4. Nella pagina del repository vuoto clicca **uploading an existing file**.
5. Trascina dentro **tutto il contenuto** della cartella `simulatore-tetto-gas` (file e cartelle `icons` e `fonts`, non la cartella stessa). Premi **Commit changes**.
6. Vai in **Settings › Pages**. Alla voce *Build and deployment* scegli **Deploy from a branch**, branch **main**, cartella **/ (root)**, poi **Save**.
7. Dopo uno o due minuti l'app è online a un indirizzo del tipo:
   `https://donato6611.github.io/simulatore-tetto-gas/`

## Versione breve da condividere su LinkedIn

Nella stessa cartella c'è `breve.html`, la versione compatta del simulatore. Una volta pubblicato il sito
è raggiungibile a un indirizzo del tipo:
`https://donato6611.github.io/simulatore-tetto-gas/breve.html`

Chiunque la apre dal link, senza account e senza installare nulla.

**Anteprima con immagine sotto il link:** in `breve.html` l'indirizzo è già impostato per l'utente
`donato6611` e il repository `simulatore-tetto-gas`. Il repository deve chiamarsi esattamente così: se usi un nome diverso,
correggi le righe `og:url` e `og:image` di `breve.html` (su GitHub: apri il file, matita, modifica, Commit changes).
Dopo la pubblicazione controlla l'anteprima su linkedin.com/post-inspector incollando l'indirizzo di `breve.html`.

**Nel post** incolla l'indirizzo di `breve.html`: LinkedIn mostra l'anteprima con l'immagine `anteprima.png`.
Se invece alleghi la tua immagine al post, l'anteprima del link non compare: in quel caso metti il link nel testo
o nel primo commento.

## Installarla sul telefono

- **Android (Chrome):** apri l'indirizzo, menu **⋮ › Installa app** (o *Aggiungi a schermata Home*). L'icona compare tra le app.
- **iPhone (Safari):** apri l'indirizzo, **Condividi › Aggiungi alla schermata Home**.

Dopo la prima apertura con connessione, l'app funziona anche offline.

## Aggiornarla

Modifica i file nel repository (per esempio carica un nuovo `index.html`), poi in `sw.js` cambia
`simulatore-tetto-v1` in `simulatore-tetto-v2`. Chi l'ha installata riceve la nuova versione alla
prima apertura con connessione (a volte serve chiudere e riaprire l'app).

## Alternativa: Netlify

Su app.netlify.com/drop trascini la cartella decompressa e ottieni subito un indirizzo.
Per tenerlo attivo nel tempo serve un account gratuito.

## Passo successivo, se vuoi Google Play

1. Con l'app già online, apri pwabuilder.com e incolla l'indirizzo.
2. Scegli il pacchetto per Android e scaricalo: contiene il file da caricare sullo store e le istruzioni.
3. Su Google Play Console servono un account sviluppatore (25 dollari una tantum) e, per gli account
   personali, un test chiuso con almeno 12 tester per 14 giorni consecutivi prima della pubblicazione.

## Privacy

L'app non raccoglie dati, non usa cookie e non carica servizi esterni: caratteri e icone sono nella cartella.
Come per qualsiasi sito, il servizio di hosting (GitHub o Netlify) può registrare dati tecnici di accesso.
