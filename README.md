# montesmedica.cz

Statický web MontesMedica s.r.o. Nasazuje se automaticky přes GitHub Pages při každém pushi do `main`
(`.github/workflows/static.yml`), doména je v souboru `CNAME`.

## Stránky

| CS | EN |
|---|---|
| `index.html` – aEyes by MontesMedica, výzkumný prototyp AI (úvodní stránka) | `en/index.html` |
| `mri.html` – připravované MR pracoviště | `en/mri.html` |
| `ochrana-osobnich-udaju.html` – ochrana osobních údajů | `en/privacy.html` |
| `aeyes.html` – jen přesměrování staré adresy na `/` | `en/aeyes.html` → `/en/` |

Každá stránka má vlastní CSS v `<head>`; společné jsou obrázky v `assets/img/` (logo, favikona, OG obrázek)
a písma v `assets/fonts/` (Cormorant Garamond a DM Sans, licence SIL OFL 1.1, načítaná lokálně přes `fonts.css`).
Při úpravě obsahu upravte vždy obě jazykové verze.

## Push jako dolomiti-mri

Repo má nastavenou lokální identitu `dolomiti-mri <dolomiti.mri@gmail.com>`. Pokud git bere jiné uložené
přihlášení, pushujte přes token z `gh` (přihlášeného jako dolomiti-mri):

```
git -c credential.helper= -c credential.helper='!gh auth git-credential' push origin main
```
