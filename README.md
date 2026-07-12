# adela — portfolio

Fotografické a filmové portfolio jako **jeden soběstačný soubor `index.html`** — CSS i JavaScript jsou vložené přímo v něm. Žádné externí soubory, žádný build. Ideální pro **GitHub Pages**.

---

## ⚠️ Oprava předchozí verze

Minule se web zobrazoval jako jeden dlouhý nenastylovaný sloupec (chybělo záhlaví, menu, zápatí). Příčina: nenačítal se externí soubor `css/style.css`. **Nová verze má styly i skript uvnitř `index.html`**, takže se to už stát nemůže.

**Co udělat:** v repozitáři nahraď starý `index.html` tímto novým. Nic víc není potřeba — složky `css/` a `js/` už web ke svému fungování nepotřebuje (můžeš je klidně smazat).

---

## Jak publikovat na GitHub Pages

1. V repozitáři nahraď soubor **`index.html`** za tuto novou verzi (musí být v **kořeni** repozitáře).
   - Přes web GitHubu: otevři repozitář → klikni na `index.html` → tužka (Edit) → smaž obsah → vlož nový → Commit. Nebo „Add file → Upload files" a přepiš.
2. Settings → **Pages** → Source: **Deploy from a branch** → branch **main**, složka **/ (root)** → **Save**.
3. Do ~1 minuty poběží na `https://adelaespresso.github.io/portfolio/`.
   - Tip: po nahrání dej v prohlížeči tvrdé obnovení (Ctrl/Cmd + Shift + R), ať se nenačte stará verze z cache.

---

## Sekce webu

Hero → **Film** (5) → **Videos** (6) → **Photography** (street/people/experimental/nature) → **Creative** (The Life of Onyxfy) → **About** → **Contact**.

Fixní záhlaví s menu, na mobilu vysouvací menu, plynulé odhalování při scrollu, lightbox u fotek, responzivní.

---

## Co doladit dál

- **Odkazy na filmy/videa:** karty ve *Film* a *Videos* teď vedou na YouTube kanál. Až budeš mít odkazy na konkrétní díla, v `index.html` uprav u dané karty `href="#"` → `href="https://…"`.
- **Obrázky:** načítají se zatím z původního Wix CDN (funguje hned). Pro plné rozlišení nezávislé na Wixu je můžeme přesunout do `assets/images/` a přepsat adresy.
- **LinkedIn:** na Wixu tam byl jen placeholder, tak jsem ho vynechal. Pošli profil a přidám ho.
- **Texty / bio:** převzaté z tvého webu, klidně uprav přímo v `index.html`.

## Vzhled (kde měnit)

Barvy a písma jsou nahoře v `<style>` v sekci `:root`:
- Paleta: espresso tmavá + teplá „papírová" bílá + tlumené mosazné akcenty.
- Písma: Fraunces (nadpisy), Inter (text), Space Mono („film slate" popisky).
