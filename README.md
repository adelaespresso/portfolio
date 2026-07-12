# adela — portfolio

Minimalistický vícestránkový web (Helvetica, černá, světlé pozadí). Každý film, video i sada fotek má **vlastní podstránku s galerií**, na kterou se proklikneš z náhledu. Fotky jsou uložené lokálně v `assets/` (nezávislé na Wixu).

## Struktura
```
index.html              home (2 obrázky přes celou šíři)
film.html               přehled filmů  → grandmas-garden.html, pigeons.html, ...
videos.html             přehled videí  → wien.html, letter-to-denmark.html, ...
photography.html        přehled fotek  → street.html, people.html, ...
creative.html           The Life of Onyxfy
contact.html            text + e-mail
<sada>.html             galerie dané sady (15 podstránek)
assets/<sada>/01.jpg…   optimalizované fotky (173 ks), 01 = titulní/náhled
.nojekyll
```

## Publikace na GitHub Pages
Souborů je teď hodně (21 stránek + 173 fotek), proto doporučuji jeden z těchto způsobů:

**A) GitHub Desktop (nejpohodlnější)**
1. Stáhni `adela-portfolio-site.zip`, rozbal.
2. V GitHub Desktop otevři repozitář `portfolio`, nakopíruj do něj obsah rozbalené složky (přepiš staré soubory).
3. Commit → Push.

**B) Přes web GitHubu**
1. Repozitář → „Add file → Upload files".
2. Přetáhni **všechny .html soubory + složku `assets` + `.nojekyll`** najednou (drag & drop zvládne i podsložky). Při velkém počtu to může chvíli trvat; když to spadne, nahraj po částech (nejdřív .html, pak složku `assets`).
3. Commit.

Pak Settings → Pages → Deploy from a branch → **main / (root)**. Po nahrání dej Ctrl/Cmd + Shift + R.

## Jak to funguje
- Náhled na `film.html` / `videos.html` / `photography.html` = titulní fotka sady (`01.jpg`); kliknutím se otevře podstránka s celou galerií.
- V galerii se kliknutím na fotku otevře velký náhled; šipkami ←/→ nebo tlačítky se listuje, Esc zavírá.

## K doladění
- **Titulní fotky** sad = zatím první fotka (`01.jpg`). Když chceš jinou, stačí ji ve složce přejmenovat na `01.jpg` (a bývalou 01 na jiné číslo), nebo mi řekni kterou.
- **Videa:** podstránky videí jsou zatím jen galerie fotek. Pošli YouTube odkazy a nahoru vložím přehrávač.
- **LinkedIn:** ikona je v záhlaví, odkaz je placeholder (`#`) — pošli URL profilu.
- **home / creative / contact:** tyto obrázky se zatím načítají z Wix CDN. Když pošleš i tyto fotky, přesunu je do `assets/` a web bude 100% nezávislý na Wixu.
