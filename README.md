# G-Procure Market Intelligence — Rinkos Rizikų Stebėjimo Skydelis

Litgrid valdymo skydelis tiekimo grandinės rinkos rizikų stebėjimui,
analizei ir sutartinių veiksmų valdymui pagal 3 lygių KPI struktūrą.

---

## Apie projektą

**Litgrid AB** — Lietuvos elektros perdavimo operatorius, pirkimus
organizuojantis pagal Lietuvos Respublikos pirkimų, atliekamų
vandentvarkos, energetikos, transporto ar pašto paslaugų srities
perkančiųjų subjektų įstatymą (PSĮ).

Skydelis skirtas Litgrid pirkimų komandai stebėti pagrindinius
rinkos rodiklius, identifikuoti tiekimo grandinės rizikas ir
priimti pagrįstus sutartinius sprendimus realiuoju laiku.

---

## KPI struktūra — 3 kategorijos / 10 rodiklių

### A — Kainos
| Rodiklis | Aprašymas |
|---|---|
| Brent | Žalios naftos kaina |
| WTI | West Texas Intermediate naftos kaina |
| LME aliuminis | Londono metalų biržos aliuminio kaina |
| LME varis | Londono metalų biržos vario kaina |
| Polimerai | Polimerinių medžiagų kainų indeksas |

### B — Lead time / pajėgumai
| Rodiklis | Aprašymas |
|---|---|
| Baltic Dry Index | Sausų birių krovinių gabenimo indeksas |
| Konteinerių frachtas | Jūrų konteinerių gabenimo kainos |
| TAC (oro kroviniai) | Oro krovinių transporto indeksas |

### C — Tiekimo nutrūkimo rizika
| Rodiklis | Aprašymas |
|---|---|
| Hormūzo tranzito indeksas | Kritinio jūrų kelio rizikos lygis |
| Sankcijų / atitikties signalai | Tiekėjų atitikties rizikos stebėjimas |

---

## Funkcionalumas

### Šviesoforo sistema
Kiekvienas rodiklis turi automatinį šviesoforo triggerį:
- Žalia — normali situacija, standartiniai veiksmai
- Geltona — stebėjimo režimas, parengtis
- Raudona — kritinis lygis, sutartiniai veiksmai

### Tendencijų analizė
- 12 savaičių tendencijų grafikas kiekvienam rodikliui
- 4 savaičių pokytis nuo bazinės reikšmės
- Bazinis sutartinis veiksmas pagal rodiklio režimą

### Kategorijų rizikos žemėlapis
Atskiras rizikos žemėlapis 5 Litgrid kategorijoms:
- Kabeliai ir laidai
- Transformatoriai / pastočių įranga
- Statyba-ranga
- IT / telekomas
- TSO atsarginės dalys

Kiekviena kategorija turi svertinį rizikos rodiklį ir konkrečius
sutartinius veiksmus pagal režimą.

### AI tendencijų santrauka
Automatiškai generuojama iš duomenų:
- Bendras rinkos klimato įvertinimas
- Didžiausi spaudimo taškai su poveikio paaiškinimu
- TSO tiekimo grandinės interpretacija:
  - Energija + logistika kyla → brangs / vėluos CAPEX
  - Oro kroviniai ↑ → rizika kritinėms dalims
  - Hormūzas → antrinė banga

### PRR kandidatai
Visi 10 rodiklių paruošti kaip PRR (Pirkimų rizikų registro)
kandidatai mėnesiniam „Rizikų registro" pildymui.

---

## Duomenų valdymas

- Rankinio redagavimo režimas — reikšmės atnaujinamos kas savaitę
- Automatinis perskaičiavimas — visi rodikliai atnaujinami iš karto
- Išsaugojimas naršyklėje — duomenys išlaikomi tarp sesijų
- Eksportas / įkėlimas — JSON formatas
- Spausdinimas į PDF — ataskaitos generavimas

SVARBU: Pradinės reikšmės yra iliustracinės. Prieš naudojant
sprendimams, jas reikia atnaujinti faktinėmis rinkos reikšmėmis
per mygtuką „Redaguoti duomenis".

---

## Techninė informacija

- Platforma — savarankiškas .html failas
- Interneto ryšys — neprivalomas (veikia offline)
- Reikalavimai — bet kokia moderni naršyklė
- Duomenys — saugomi tik naršyklėje (localStorage)

---

## Teisinė bazė

- LR Pirkimų, atliekamų vandentvarkos, energetikos, transporto ar
  pašto paslaugų srities perkančiųjų subjektų įstatymas (PSĮ)
- Litgrid AB vidinės pirkimų procedūros ir rizikų valdymo gairės

---

## Failai

| Failas | Aprašymas |
|---|---|
| `index.html` | Pagrindinis skydelio failas |
| `README.md` | Projekto aprašymas |

---

## G-Procure ekosistema

| Įrankis | Nuoroda |
|---|---|
| G-Procure Home | https://Jurgelaitis.github.io/PP-home/G-Procure_Home.html |
| G-Procure Planner | https://Jurgelaitis.github.io/PP-Planing/EPSO-G_pirkimu_planavimas_MVP.html |
| G-Procure Advisor | https://Jurgelaitis.github.io/PP-TS/TS_Asistentas.html |
| G-Procure Negotiator | https://Jurgelaitis.github.io/PP-Negotation/EPSO-G_Derybu_Pasirengimo_Irankis.html |
| G-Procure Evaluator | https://Jurgelaitis.github.io/PP-Test/litgrid-vertinimo-irankis.html |

---

## Statusas

Veikianti versija — duomenis atnaujinti prieš naudojimą

## Atsakingas

Arunas Jurgelaitis — Head of Procurement, Litgrid AB

---

G-Procure — Intelligent Procurement for EPSO-G Group
