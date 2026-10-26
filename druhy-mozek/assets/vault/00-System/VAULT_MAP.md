# VAULT_MAP: mapa a pravidla vaultu

*Založeno: {{DATUM}} • Zdroj pravdy o struktuře. Workflow → [[SKILL_MAP]]*

## Struktura

### 00-System: řízení a pravidla
- [[MI]]: kdo jsem, kde pracuju, jak se rozhoduju, rozhodovací filtr
- [[CLAUDE_RULES]]: jak se mnou Claude pracuje (sbírané korekce)
- [[JAK_MLUVIT_S_CLAUDEM]]: denní vstup, vodítka, užitečné věty
- [[ULOHY]]: zadání úloh (ranní zpracování, review, údržba, digest)
- [[BRIEF]]: ranní brief (přepisuje se každé ráno)
- [[DASHBOARD]]: stav na jedné stránce (přepisuje se při review)
- [[Cile]]: teď / pak / dlouhodobě + aktuální kvartál
- [[Decision_Log]]: zásadní rozhodnutí s důvodem
- [[Tydenni_Review]]: šablona týdenního review
- [[VSTUP_STAV]]: které nahrávky, maily a přepisy už jsou zpracované
- [[SETUP]]: jak a kdy vznikl tenhle druhý mozek
- `Vault_Health.md`: report údržby (vzniká sám, přepisuje se)
- `CLAUDE.md` (v kořeni): instrukce pro Clauda

### 05-Inbox: vstupní brána
Všechno nezařazené. Třídit min. 1× týdně (součást review).
- `Prepisy/`: přepisy schůzek ke zpracování (ranní zpracování je vezme)
- `Sliby_k_zarazeni.md`: sliby k lidem bez karty (vzniká sám, review je
  rozřadí)

### 10-Firmy: firmy a organizace
1 soubor na firmu (šablona `Firma`), název malými bez diakritiky
(`acme.md`). Pole `vztah`: `moje` (vedu nebo vlastním), `zamestnavatel`,
`klient` (klíčový klient s víc zakázkami), `partner`. Co firma dělá,
moje role, lidi, kde se vede obchod a účetnictví, historie.

### 15-Zakazky: zakázky a obchod
- 1 soubor na zakázku nebo obchodní příležitost:
  `Zakazka_<Klient>_<Nazev>.md` (šablona `Zakazka`), stav ve frontmatteru
- přehled: `Zakazky.base`
- **Dvě zakázky u jednoho klienta = dva soubory.**
- Kde se obchod vede: {{KDE_OBCHOD}}

### 20-Lide: lidi
1 soubor na člověka (šablona `Kontakt`), název `Jmeno_Prijmeni.md` bez
diakritiky. Kdo to je, odkud se známe, sliby, propojení, historie.
Přehled `Lide.base`.

### 25-Schuzky: zápisy ze schůzek
`Schuzka_<Kdo>_RRRR-MM-DD.md` (šablona `Schuzka`). Zdroj: nahrávka,
přepis online callu, vlastní poznámky.

### 30-Projekty: projekty
Projekty s cílem a koncem (šablona `Projekt`): pracovní (zadané v práci)
i vlastní. Nový vlastní projekt jen přes filtr z [[MI]]. Přehled
`Projekty.base`.

### 40-Znalosti: trvalé know-how
Obor, trh, nástroje, rešerše, poznatky. `Digest/`: ranní digesty (když
běží).

### 50-Osobni: osobní (CITLIVÉ)
- `Denik/`: denní zápisy `RRRR-MM-DD.md`, review `RRRR-Wxx.md` / `RRRR-MM.md`
- `Setup/`: rozhovor ze setupu druhého mozku
- Další osobní věci: {{OSOBNI}}

### 60-Assets: podklady
- `Templates/`: šablony (Firma, Kontakt, Zakazka, Schuzka, Projekt)

### 90-Archiv: ukončené
Hotové zakázky a projekty, vytěžené rozhovory. Nic se nemaže.

## Pravidla

1. Nezařazené → `05-Inbox`, třídit min. 1× týdně
2. Hotová zakázka nebo projekt → poznatek do `40-Znalosti`, soubor do `90-Archiv`
3. Časově citlivé vždy s datem
4. Nikdy nemazat bez potvrzení, přesouvat do `90-Archiv`
5. Citlivé: celá `50-Osobni/`, [[MI]], [[Decision_Log]] a {{CITLIVE}}.
   Nikdy do výstupů pro klienty, prezentací, veřejných textů ani zpráv
   pro tým
6. Linkovat wikilinky, souvislosti jsou polovina hodnoty vaultu
7. Podsložka vzniká, až do ní padá třetí soubor stejného druhu
   (u `25-Schuzky` až nad 30 souborů, pak po měsících `RRRR-MM/`)

## Pojmenování

- Nové soubory bez diakritiky a bez mezer
- Datované záznamy `RRRR-MM-DD[-slug].md`, týdny `RRRR-Wxx.md`, měsíce `RRRR-MM.md`
- Pojmenované záznamy s datem na konci: `Typ_Nazev_RRRR-MM-DD.md`
- Dokumenty pro klienty vždy s datem nebo verzí v názvu
  (`Nabidka_Klient_RRRR-MM-DD.pdf`, druhá verze týž den `_v2`)
- Druhá schůzka se stejným člověkem týž den: přípona `-2`

## Frontmatter

| Pole | Kdo ho má | Hodnoty |
|---|---|---|
| `typ` | každá entita | `firma` / `zakazka` / `kontakt` / `schuzka` / `projekt` / `report` / `digest` |
| `firma` | zakázka, projekt, schůzka | slug mojí firmy nebo zaměstnavatele = název souboru v `10-Firmy` (pod kterou mojí rolí to běží) |
| `firma` | kontakt | kde ten člověk pracuje (slug, když má soubor v `10-Firmy`, jinak název) |
| `vztah` | firma | `moje` / `zamestnavatel` / `klient` / `partner` |
| `stav` | zakázka | `rozjednano` / `nabidka` / `bezi` / `pozastaveno` / `hotovo` / `prohrano` |
| `stav` | projekt | `aktivni` / `pozadi` / `parkovano` / `hotovo` |
| `stav` | firma | `aktivni` / `utlum` / `neaktivni` |
| `klient` | zakázka | název klienta |
| `vede_se` | zakázka | `vault` (stav tady) / `crm` (stav v systému, kde pracují i jiní; tady jen poznámky) |
| `ceka_na` | zakázka, projekt | `ja` / `klient` / jméno malými bez diakritiky (`petr`) / `nikdo` |
| `termin` | zakázka, projekt | RRRR-MM-DD; `ceka_na: ja` **musí** mít termín |
| `dalsi_krok` | zakázka, projekt | jedna věta |
| `hodnota` | zakázka | Kč bez DPH, číslo |
| `posledni_kontakt` | zakázka, kontakt | RRRR-MM-DD |
| `role` | kontakt | role toho člověka jednou dvěma slovy |
| `udrzovat` | kontakt | `ano` / `ne` (jestli hlídat, že spolu dlouho nemluvíme) |
| `datum` | schůzka | RRRR-MM-DD |
| `zdroj` | schůzka | `plaud` / `prepis` / `poznamky` |
| `aktualizovano` | firma, projekt | datum poslední revize |

**Hodnoty polí malými písmeny a bez diakritiky** (`ja`, ne `já`).
Přehledy a úlohy porovnávají přesně, jinak záznam z pohledu zmizí.
Nové pole vzniká, jen když ho něco čte (přehled `.base`, úloha).

## Řádky slibů

Sliby se píšou jako úkol (checkbox) do sekce `## Sliby` u člověka
(slib klientovi bez jména u zakázky, jinak u firmy), vždy s datem:

```
- [ ] já → [[Petr_Novak]]: poslat nabídku na školení · do 2026-10-24
- [ ] [[Petr_Novak]] → já: rozhodnutí o pilotu · do 2026-10-31
```

Splněno = zaškrtnout a připsat datum (`✓ 2026-10-23`). Ranní zpracování
a review hledají řádky `- [ ]` v sekcích `## Sliby` napříč `20-Lide`,
`15-Zakazky`, `30-Projekty`, `10-Firmy` a v `05-Inbox/Sliby_k_zarazeni.md`.
V deníku se sliby jen odkazují, bez zaškrtávacích políček.
