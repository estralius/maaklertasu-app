# Maaklertasu app

Maaklertasu ja notaritasu kalkulaator Eesti maakleritele.

## Failid

- `index.html` - põhirakendus (HTML + CSS + JS ühes failis)
- `manifest.json` - PWA metaandmed
- `sw.js` - service worker (offline tugi)
- `icon-192.png`, `icon-512.png` - app ikoonid

## Tehnoloogia

- Puhas HTML, CSS ja JavaScript - **ei vaja build-protsessi**
- PWA (paigaldatav telefoni)
- Töötab offline (peale esimest külastust)
- Mobile-first disain

## Local arendamine

Lihtsalt ava `index.html` brauseris või kasuta lihtsat HTTP serverit:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve
```

Mine `http://localhost:8000` brauseris.

## Deploy

Push muudatused GitHubi - Cloudflare Pages teeb deploy automaatselt.

**Tähtis:** kui muudad `sw.js` faili, suurenda `CACHE_VERSION` numbrit (`v1` → `v2`), 
muidu kasutajate brauserid kasutavad vana cache'itud versiooni.

## Allikad

- Notaritasude tabel: Notari tasu seaduse § 22 (kehtiv 1.03.2025)
- Riigilõivud: Riigilõivuseaduse Lisa 2 (kehtiv 1.01.2025)
- Käibemaks: 24% (kehtiv alates 1.07.2025)
