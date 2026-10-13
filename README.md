# montesmedica.cz

Statický web MontesMedica s.r.o. Nasazuje se automaticky přes GitHub Pages při každém pushi do `main`
(`.github/workflows/static.yml`), doména je v souboru `CNAME`.

## Stránky

| CS | EN |
|---|---|
| `index.html` – MR pracoviště (úvodní stránka) | `en/index.html` |
| `mri.html` – jen přesměrování staré adresy na `/` | `en/mri.html` → `/en/` |
| `aeyes.html` – jen přesměrování staré adresy na `/` | `en/aeyes.html` → `/en/` |

Stránka aEyes je zatím skrytá (říjen 2026). Poslední verze je v commitu `ff2e078`
(`index.html`, `en/index.html`). Vrátit ji lze např. `git show ff2e078:index.html > aeyes.html`
a `git show ff2e078:en/index.html > en/aeyes.html`, pak odkomentovat odkaz `nav-aeyes` v obou `index.html`.

Každá stránka má vlastní CSS v `<head>`; společné jsou jen obrázky v `assets/img/` (logo, favikona, OG obrázek).
Při úpravě obsahu upravte vždy obě jazykové verze.

## Push jako dolomiti-mri

Repo má nastavenou lokální identitu `dolomiti-mri <dolomiti.mri@gmail.com>`. Pokud git bere jiné uložené
přihlášení, pushujte přes token z `gh` (přihlášeného jako dolomiti-mri):

```
git -c credential.helper= -c credential.helper='!gh auth git-credential' push origin main
```
