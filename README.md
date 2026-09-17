# montesmedica.cz

Statický web MontesMedica s.r.o. Nasazuje se automaticky přes GitHub Pages při každém pushi do `main`
(`.github/workflows/static.yml`), doména je v souboru `CNAME`.

## Stránky

| CS | EN |
|---|---|
| `index.html` – MR pracoviště | `en/index.html` |
| `aeyes.html` – aEyes, AI expertní systémy | `en/aeyes.html` |

Každá stránka má vlastní CSS v `<head>`; společné jsou jen obrázky v `assets/img/` (logo, favikona, OG obrázek).
Při úpravě obsahu upravte vždy obě jazykové verze.

## Push jako dolomiti-mri

Repo má nastavenou lokální identitu `dolomiti-mri <dolomiti.mri@gmail.com>`. Pokud git bere jiné uložené
přihlášení, pushujte přes token z `gh` (přihlášeného jako dolomiti-mri):

```
git -c credential.helper= -c credential.helper='!gh auth git-credential' push origin main
```
