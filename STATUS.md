# STATUS — asiakastarinat

Päivitetty: 2026-09-08 13:10

## Kesken nyt

**Siskon Siivous — tarina lähetetty 8.9.2026 asiakkaalle ja Pialle tarkistettavaksi.**
1 662 sanaa, kolme haastateltavaa *(Robert Tedre, Vesa Fagerlund, Sara Koskivirta)*.
Luonnos viimeisteltiin ChatGPT:ssä promptilla `hailer-gtm/PROMPT_ASIAKASTARINAN_VIIMEISTELY.md`.
Lähetetty versio talteen: `hailer-gtm/TARINA_SISKON_SIIVOUS_LAHETETTY.md`.

🔴 **Sivua ei tehdä eikä tekstiä viedä tähän repoon ennen hyväksyntää** — tämä repo
julkaisee `hailerreferences.com`-sivuston.

Tiedossa oleva jatkosuunnitelma: **Lamor osa 2 -asiakastarina Anishista.** Lamorin
sisällä neljä ihmistä rakentaa omia työkalujaan Hailerilla (Anish, Mari, Marco,
William) — se on vastaus kysymykseen "kenelle Hailer 1.0 on".

Viimeisin commit (4f1f933) lisäsi Google Search Console -vahvistustunnisteen.

## Seuraava askel

**1. Odota asiakkaan ja Pian kommentit** Siskon Siivouksen tarinaan.

**2. Kun hyväksytty: tee `tarinat/siskon-siivous.html`** pohjasta `malli.html` ja aja
menetelmän vaihe 6 — vakiokuvaus sanasta sanaan samana kolmessa paikassa *(näkyvä
teksti, `llms.txt`, JSON-LD)*, `Article` + `about: Organization`, neljä kuvaviittausta,
ja `sitemap.xml`:n päivitys.

**3. Kysy Robertilta lupa yhteen sitaattiin** jos se palaa tekstiin: *«…paskat
housussa, sanotaanpa näin»*. Sitä ei siistitä meidän päätöksellä.

**4. Varmista Sara Koskivirran sukunimen kirjoitusasu** — litterointi mankeloi sen
muotoon *«Siska Rakoski Virta»*.

## Odottaa

- **Pääkuvan isompi versio** — pyydetty markkinoinnista 8.9. *(Jaana 8.9.)*.
  Tiedosto `_93A0220.JPG`, nykyinen 1024 × 683, **tarvitaan vähintään 1200 px**
  koska sama kuva menee `og:image`-jakokuvaksi. Henkilökuvia ei pyydetty uusiksi —
  ne ovat kunnossa pieninä.
  todenna: `python3 -c "from PIL import Image; print(Image.open('kuvat/siskon-siivous-hero.jpg').size)"` → ≥1200 = tullut
- **Siskon Siivouksen hyväksyntä** — tarina lähetetty 8.9.2026 asiakkaalle ja Pialle
  *(Jaana 8.9.)*. Haastatteluaineisto on koossa: Robert, Vesa, Sara.
  todenna: `ls hailer-gtm/TARINA_SISKON_SIIVOUS_LAHETETTY.md`

## Päätökset joita ei saa perua

- **Asiakas on sankari, ei Hailer.** Tarinaa ei arvioida tuote-esitteenä.
- **Lähteitä on vain kaksi:** mitä haastattelussa sanottiin ja mitä yritys itse
  kertoo verkkosivullaan. Taustatutkimus on kysymyksiä varten, ei tekstiä varten.
- **Ei ylimääräisiä lupakierroksia.** Haastateltavat tietävät itse organisaationsa
  hyväksymisreitit.
- Google Analytics poistettu, Vercel Insights jää (commit 3c5c344).

## Viitteet

- GitHub: `HailerOy/hailerreferences`
- `hailer-gtm/SISKON_SIIVOUS_SITAATIT.md` — sanatarkka sitaattiarkisto, tarinan lähde
- `hailer-gtm/HAASTATTELURUNKO.md`
