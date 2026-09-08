# CLAUDE.md — asiakastarinat (hailerreferences.com)

Tekninen totuus tästä reposta: **miten tämä sivusto toimii ja miten sitä muokataan.**
Säännöt ovat `~/Hailer/CONTEXT.md`:ssä, tila `STATUS.md`:ssä — ei täällä.

## Mikä tämä on

Hailerin asiakasreferenssisivusto. **Staattinen HTML, ei buildia, ei riippuvuuksia.**
Muokkaat tiedostoa ja se on valmis — ei `npm install`, ei käännösvaihetta.

- **Julkaistu:** `https://www.hailerreferences.com` (Vercel)
- **GitHub:** `HailerOy/hailerreferences`
- **Julkaisu:** push `main`-haaraan → Vercel julkaisee automaattisesti

## Rakenne

```
index.html            etusivu, tarinakortit
tarinat/
  malli.html          ⭐ POHJA uudelle tarinalle — ei julkaistava sivu
  kirbeto.html        Kirbeto Oy
  kspt-group.html     KSPT Group Oy
  viestinta-ruuti.html Viestintä Ruuti Oy
kuvat/                hero- ja korttikuvat, hailer-logo.png
llms.txt              koneluettava kuvaus tekoälyhakua varten
sitemap.xml robots.txt favicon.svg favicon-32.png apple-touch-icon.png
```

`malli.html` on **pohja, ei sivu.** Siinä on `noindex`, ja se on tarkoituksella pois
sitemapista. Uusi tarina tehdään kopioimalla se — älä kirjoita tarinasivua tyhjästä.

## Uuden asiakastarinan lisääminen — kaikki viisi kohtaa

Tarina ei ole valmis ennen kuin **kaikki** nämä on tehty. Kolme ensimmäistä on helppo
muistaa, kaksi viimeistä unohtuu:

1. `cp tarinat/malli.html tarinat/<asiakas>.html` ja täytä sisältö
2. **Poista `noindex`** kopiosta — muuten sivu ei koskaan näy haussa
3. Lisää hero- ja korttikuva `kuvat/`-kansioon
4. Lisää kortti `index.html`:n tarinalistaan
5. Lisää **`sitemap.xml`:ään** *(`<loc>`, `<lastmod>`, `priority` 0.8)* **ja
   `llms.txt`:ään** *(rivi muotoa: yritys — toimiala. Yhden virkkeen kuvaus. URL)*

⚠️ `llms.txt` on se tiedosto jonka kautta tekoälyhaku löytää tarinat. **Jos tarinaa ei
lisätä sinne, se on olemassa vain ihmisille.**

## Konventiot joita ei muuteta ilman syytä

| | |
|---|---|
| Fontti | Nunito, Google Fontsista |
| Analytiikka | **Vercel Insights** (`/_vercel/insights/script.js`). ⚠️ Google Analytics poistettiin tarkoituksella (commit `3c5c344`) — älä lisää takaisin |
| Rakennedata | Jokaisella sivulla `application/ld+json` JSON-LD -lohko |
| Alatunniste | Hailerin vakiokuvaus. **Lähde on `~/Hailer/hailer-gtm/KUVAUS_HAILER.md` — kopioi sieltä, älä muotoile uudelleen** |
| Kieli | Sivusto on suomeksi |

## Salaisuudet

`.env.local` sisältää Vercelin oman `VERCEL_OIDC_TOKEN`-tunnisteen. Se on `.gitignore`ssa
(`.env*`) eikä ole koskaan ollut historiassa — **tarkistettu 30.8.2026.** Pidä näin.

## Tarkistettu 30.8.2026

- `.gitignore` kattaa `.DS_Store`, `.vercel`, `.env*` ✅
- `malli.html`:ssä on `noindex` ✅
- Sitemapissa 4 osoitetta: etusivu + kolme tarinaa ✅
