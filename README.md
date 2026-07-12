# adela — portfolio

Statické (čistě HTML/CSS/JS) fotografické a filmové portfolio připravené k publikaci na **GitHub Pages**.

Žádné frameworky, žádný build. Stačí nahrát soubory na GitHub a zapnout Pages.

---

## Struktura

```
adela-portfolio/
├── index.html          # celý web (jedna stránka se sekcemi)
├── css/style.css       # vzhled
├── js/main.js          # menu, animace, lightbox
├── assets/images/      # sem dej vlastní fotky (viz níže)
├── .nojekyll           # ať GitHub Pages nic nepřepisuje
└── README.md
```

Sekce: **Hero → Film → Videos → Photography → Creative → About → Contact**.

---

## Jak to publikovat na GitHub Pages

1. Na [github.com](https://github.com) vytvoř nový **veřejný** repozitář (např. `portfolio`).
2. Nahraj do něj **obsah složky `adela-portfolio`** — tedy `index.html`, složky `css/`, `js/`, `assets/` a soubor `.nojekyll`. Důležité: `index.html` musí být v **kořeni** repozitáře, ne ve vnořené složce.
   - Přes web: „Add file → Upload files" a přetáhni soubory.
   - Nebo přes příkazovou řádku:
     ```bash
     git init
     git add .
     git commit -m "portfolio"
     git branch -M main
     git remote add origin https://github.com/UZIVATEL/portfolio.git
     git push -u origin main
     ```
3. V repozitáři jdi do **Settings → Pages**.
4. U „Build and deployment" zvol **Source: Deploy from a branch**, branch **main**, složka **/ (root)**, a dej **Save**.
5. Za chvíli (do ~1 min) bude web na adrese:
   `https://UZIVATEL.github.io/portfolio/`

> Chceš vlastní doménu (např. `adela.film`)? V Settings → Pages je pole „Custom domain".

---

## Co ještě doladit (dělali jsme to jako základ)

**1) Odkazy na filmy a videa**
Karty ve `Film` a `Videos` teď vedou na YouTube kanál. Až budeš mít odkazy na konkrétní filmy (YouTube/Vimeo), stačí v `index.html` u dané karty upravit `href="#"` → `href="https://…"`.

**2) Obrázky**
Fotky se teď načítají z původního Wix CDN (`static.wixstatic.com`) — web tedy funguje hned. Až budeš chtít vlastní hostování (nezávislé na Wixu a v plném rozlišení):
- nahraj obrázky do `assets/images/`,
- v `index.html` nahraď dlouhé `https://static.wixstatic.com/...` adresy za `assets/images/nazev.jpg`.

**3) LinkedIn**
Na původním webu byl u LinkedInu placeholder odkaz, tak jsem ho vynechal. Když pošleš svůj profil, přidám ho do sekce Contact.

**4) Texty**
Bio v sekci *About* je převzaté z tvého webu. Klidně uprav přímo v `index.html`.

---

## Vzhled

- **Paleta:** espresso tmavá + teplá „papírová" bílá + tlumené mosazné (tungsten) akcenty.
- **Písma:** Fraunces (nadpisy, literární serif), Inter (text), Space Mono („film slate" popisky).
- **Detaily:** jemný filmový grain, plynulé odhalování při scrollu, lightbox u fotek, responzivní menu.

Barvy a písma se dají měnit nahoře v `css/style.css` v sekci `:root`.
