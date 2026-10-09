# Sito Alessio Melia

File: `index.html` (sito), `admin.html` (pannello), `data.json` (contenuti), cartella `img/` (miniature e loghi, da creare).

## Pubblicare su GitHub Pages
1. Crea un account su github.com e un repository pubblico (es. `portfolio`).
2. Carica tutti i file (Add file > Upload files), inclusa la cartella `img/`.
3. Settings > Pages > Source: "Deploy from a branch", branch `main`, cartella `/ (root)`.
4. Dopo circa un minuto il sito è su `https://TUOUTENTE.github.io/portfolio/`.

## Usare il pannello
1. Apri `.../admin.html`.
2. Modifica progetti, servizi, clienti. Le modifiche restano come bozza nel browser.
3. "Pubblica su GitHub": inserisci utente, repository e un token, oppure "Scarica data.json" e caricalo a mano nel repository.

Token: GitHub > Settings > Developer settings > Fine-grained tokens. Limitalo al solo repository del sito, con permesso "Contents: Read and write".

## Dominio
1. Compra il dominio (Cloudflare Registrar, Namecheap, Porkbun o Aruba per .it).
2. In Settings > Pages > Custom domain inserisci il dominio e attiva "Enforce HTTPS".
3. Nel DNS del dominio: quattro record `A` verso `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` e un `CNAME` per `www` verso `TUOUTENTE.github.io`. Verifica gli indirizzi nella documentazione GitHub Pages prima di configurare.

## Provare in locale
Il sito legge `data.json`, quindi va aperto da un server: nella cartella lancia `python3 -m http.server` e visita `http://localhost:8000`.
