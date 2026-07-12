# adela — portfolio

Věrná minimalistická kopie webu (světlý vzhled), rozdělená na **samostatné stránky** jako originál:
`home · film · videos · photography · creative · contact`.

Každá stránka je **soběstačný HTML soubor** (styl i skript uvnitř) — žádné externí `css/`/`js/` složky, nic se nemůže „nenačíst".

## Soubory
```
index.html          (home)
film.html
videos.html
photography.html
creative.html
contact.html
.nojekyll
```

## Publikace na GitHub Pages
1. Nahraj **všech 6 .html souborů + .nojekyll** do **kořene** repozitáře `portfolio` (žádné podsložky).
   - Přes web: repozitář → „Add file → Upload files" → přetáhni všechny soubory → Commit.
2. Settings → **Pages** → Source: **Deploy from a branch** → branch **main**, složka **/ (root)** → Save.
3. Web poběží na `https://adelaespresso.github.io/portfolio/`.
4. Po nahrání dej tvrdé obnovení (Ctrl/Cmd + Shift + R), ať se nenačte stará verze z cache.

Menu nahoře prokliká jednotlivé stránky, aktivní stránka je podtržená.

## K doladění
- **Odkazy na filmy/videa:** karty vedou zatím na YouTube kanál; u `film.html`/`videos.html` stačí změnit `href` na konkrétní díla.
- **Obrázky:** načítají se z původního Wix CDN (funguje hned).
- **LinkedIn:** na originále byl jen placeholder, tak vynechán — pošli profil a přidám.

## Vzhled
Bílé pozadí, černý text, čisté písmo Inter, prokliky s podtržením, u fotek a Onyxfy lightbox. Barvy/písmo se mění nahoře v `<style>` (`:root`).
