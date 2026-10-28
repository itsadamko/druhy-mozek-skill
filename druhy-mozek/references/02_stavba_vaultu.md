# Stavba vaultu

## Struktura

```
Vault/
├── CLAUDE.md                     ← instrukce pro Clauda (role, tón, pravidla)
├── 00-System/                    ← řízení a pravidla
│   ├── VAULT_MAP.md              ← mapa a pravidla vaultu
│   ├── SKILL_MAP.md              ← workflow (denní vstup, schůzky, lidi, sliby, zakázky, review)
│   ├── MI.md                     ← kdo jsem, kde pracuju, rozhodovací filtr
│   ├── CLAUDE_RULES.md           ← korekce, jak se mnou pracovat
│   ├── JAK_MLUVIT_S_CLAUDEM.md   ← denní vstup, vodítka, užitečné věty (tahák)
│   ├── ULOHY.md                  ← zadání všech úloh (ranní zpracování, review, údržba, digest)
│   ├── BRIEF.md                  ← ranní brief (přepisuje ho ranní zpracování)
│   ├── DASHBOARD.md              ← stav na jedné stránce (přepisuje se v review)
│   ├── Cile.md                   ← teď / pak / dlouhodobě + kvartál
│   ├── Decision_Log.md           ← zásadní rozhodnutí
│   ├── Tydenni_Review.md         ← šablona týdenního review
│   ├── VSTUP_STAV.md             ← které nahrávky, maily a přepisy už jsou zpracované
│   └── SETUP.md                  ← stav setupu
├── 05-Inbox/                     ← všechno nezařazené
│   └── Prepisy/                  ← sem se ukládají přepisy schůzek ke zpracování
├── 10-Firmy/                     ← 1 soubor na firmu (moje, zaměstnavatel, klíčoví klienti)
├── 15-Zakazky/                   ← zakázky a obchodní příležitosti
│   └── Zakazky.base              ← přehled (Obsidian Bases)
├── 20-Lide/                      ← lidi: 1 soubor na člověka
│   └── Lide.base                 ← přehled lidí a posledních kontaktů
├── 25-Schuzky/                   ← zápisy ze schůzek
├── 30-Projekty/                  ← projekty s cílem a koncem (pracovní i vlastní)
│   └── Projekty.base
├── 40-Znalosti/                  ← trvalé know-how, rešerše, digesty
├── 50-Osobni/                    ← CITLIVÉ: deník, osobní věci
│   ├── Denik/
│   └── Setup/                    ← vytěžený rozhovor ze setupu (fáze 5)
├── 60-Assets/
│   └── Templates/                ← Firma, Kontakt, Zakazka, Schuzka, Projekt
└── 90-Archiv/                    ← ukončené (nic se nemaže)
```

Prázdné složky založ taky, i `15-Zakazky/` u člověka bez obchodu (ať jde
kdykoli začít). Podsložky uvnitř vznikají až u třetího souboru stejného
druhu, u schůzek až když je jich ve složce přes 30.

## Postup

1. Zkopíruj `assets/vault/` do kořene vaultu (zachovej strukturu).
   `00-System/SETUP.md` už obvykle existuje z fáze 0, pak ho přeskoč.
   Soubor po souboru, před každým zápisem ověř, že cílový soubor
   neexistuje. `BRIEF.md` a `VSTUP_STAV.md` jsou prázdné kostry, plní je
   ranní zpracování. Šablona týdenního review je výjimečně
   v `00-System/Tydenni_Review.md` (ne v `60-Assets/Templates`).
2. Vyplň `{{…}}` podle tabulky níže. Formulace z rozhovoru ber jeho
   slovy, kde na nich záleží (cíle, rizika, tón, vodítka). **Mluvnický
   rod** v šablonách je mužský („slíbil jsem“, „sám sobě“): u ženy ho
   uprav (vzory v `JAK_MLUVIT_S_CLAUDEM.md`, `ULOHY.md`, `CLAUDE.md`).
3. **Volitelné bloky** v `ULOHY.md`, `SKILL_MAP.md` a
   `JAK_MLUVIT_S_CLAUDEM.md` jsou ohraničené řádky `[POKUD X]` a
   `[/POKUD]`. Bloky, které platí, nech a smaž jen ty dva řádky se
   značkami. Bloky, které neplatí, smaž celé i se značkami. Značky:
   - `[POKUD PLAUD]`, `[POKUD MAIL]`, `[POKUD CHECKIN]`: podle G1 (může
     platit víc naráz)
   - `[POKUD VIC]`: profil VÍC (víc firem nebo rolí)
   Když se cesta vstupu později změní (fáze 3 nebo vyhodnocení
   tréninku), blok se vrátí ze šablony v `assets/vault/`. Složka
   `05-Inbox/Prepisy/` a její zpracování platí vždycky (záloha pro
   přepisy, které nejdou přes konektor).
   Sekce úloh v `ULOHY.md` (review, údržba, digest) zůstávají vždycky:
   na slovo jdou spustit kdykoli. G8 rozhoduje jen o tom, které poběží
   automaticky.
4. Zakládej rovnou:
   - **Firmy z A2** do `10-Firmy/` ze šablony Firma (`vztah: moje` nebo
     `zamestnavatel`). Název souboru malými bez diakritiky (`acme.md`,
     `novak-consulting.md`). Freelancer bez firmy: jeden soubor se jménem
     jeho podnikání (`ja-freelance.md` nebo značka, pod kterou fakturuje).
     Klíčové klienty jen když o nich mluvil jako o vztahu (`vztah: klient`).
   - **Lidi z B1** do `20-Lide/` ze šablony Kontakt. Jen to, co řekl.
   - **Rozjeté zakázky z A3 a C1** do `15-Zakazky/` ze šablony Zakazka
     (`Zakazka_<Klient>_<Nazev>.md`), `vede_se: vault`. Když dal do
     `05-Inbox/` vlastní tabulku zakázek (C1), založ zakázky z ní, ukaž
     mu seznam ke kontrole a tabulku nech, kde je. Když zakázky vede
     v systému, kde pracují i jiní, soubor zakládej jen pro ty, ke kterým
     si chce vést vlastní poznámky, s `vede_se: crm` a bez stavových
     polí (jen odkaz, kde žije).
   - **Projekty z A3** do `30-Projekty/` ze šablony Projekt. Pracovní
     projekty (zadané v práci) bez filtru; vlastní nové nápady jen po
     filtru z `MI.md`, co neprojde, jde do `05-Inbox/`.
   - Prázdné `05-Inbox/Prepisy/`, `25-Schuzky/`, `40-Znalosti/`,
     `50-Osobni/Denik/`, `50-Osobni/Setup/`, `90-Archiv/`.
   - `05-Inbox/Sliby_k_zarazeni.md` se nezakládá předem, vznikne sám
     (workflow 3).
5. `{{TRENINK_DO}}` vyplň textem `(nastaví se ve fázi 4)`. Řádek
   `Start:` do `VSTUP_STAV.md` a skutečné datum konce tréninku se
   zapisují až ve fázi 4, těsně před zkušebním vstupem.
6. Kontrola: `grep -rn "{{" .` a `grep -rn "\[POKUD\|\[/POKUD" .` ve vaultu
   nesmí nic najít.
7. Kontrola wikilinků: každý `[[cíl]]` v nových souborech musí existovat
   jako soubor (kromě záměrně budoucích, ty přepiš na prostý text).
   Příklady v blocích kódu (třeba `[[Petr_Novak]]` ve `VAULT_MAP.md`)
   nejsou odkazy, nech je být.

## Mapování rozhovoru na šablony

| Místo | Odkud | Kam |
|---|---|---|
| `{{DATUM}}` | `date +%F` | všude |
| `{{VAULT_CESTA}}` | cesta, jak ji vidí počítač (`/Users/jana/Vault`, `C:\Users\jana\Vault`), nikdy `/sessions/…` | `CLAUDE.md`, `ULOHY.md`, `SETUP.md` |
| `{{APPKA}}` | fáze 0, krok 1: `Claude Cowork` / `ChatGPT Work` | `SETUP.md` |
| `{{JMENO}}` | jak mu říkat (křestní jméno) | `CLAUDE.md`, `ULOHY.md` |
| `{{OSLOVENI}}` | začátek setupu: „Tykej mi“ / „Vykej mi“ | `CLAUDE.md` Tón |
| `{{ROLE_VETA}}` | A1 | `CLAUDE.md`, `MI.md`, `ULOHY.md` (digest) |
| `{{FIRMY}}` | A2: odrážka na firmu nebo roli (wikilink na soubor v `10-Firmy`, role, co dělá, % času) | `MI.md` |
| `{{PRACE_TED}}` | A3 | `MI.md`, `DASHBOARD.md` |
| `{{VLASTNI_PROCES}}` | A4 krok po kroku. Když žádný není: „(zatím žádný)“ | `SKILL_MAP.md` workflow 10 |
| `{{UDRZOVAT_DNI}}` | B3 (číslo, výchozí 60) | `SKILL_MAP.md`, `ULOHY.md` |
| `{{KDE_OBCHOD}}` | C1 (blok C přeskočen: „zakázky ani obchod nevedu“) | `SKILL_MAP.md` workflow 5, `VAULT_MAP.md` |
| `{{CENA_SMLOUVY}}` | C2 (bez obchodu: „netýká se mě“) | `CLAUDE_RULES.md` |
| `{{CIL_TED}}`, `{{CIL_PAK}}`, `{{CIL_DLOUHODOBE}}` | D1 | `Cile.md`, `MI.md` |
| `{{HLAVNI_PRIORITA}}` | D2 | `MI.md` |
| `{{KVARTAL}}` | aktuální kvartál z data (např. `Q4 2026`) | `Cile.md` |
| `{{CILE_KVARTAL}}` | D1 „teď“ rozepsané na 1 až 3 měřitelné cíle | `Cile.md` |
| `{{PREFERENCE}}` | E1 jako číslovaný seznam | `MI.md` |
| `{{HLAVNI_RIZIKO}}` | E2, krátce | `CLAUDE.md` |
| `{{RIZIKA}}` | E2 rozepsané, odrážky | `MI.md` |
| `{{FILTR_PODMINKY}}` | E3, číslovaný seznam | `MI.md` |
| `{{FILTR_POJISTKA}}` | E3 pojistka | `MI.md` |
| `{{TON}}` | F1, dvě až tři věty popisu | `CLAUDE.md` |
| `{{MENTOR_HLIDA}}` | F2 | `CLAUDE.md`, instrukce projektu |
| `{{TECHNIKA}}` | F3 jednou větou | `CLAUDE.md` |
| `{{VSTUP}}` | G1 krátce: „hlasovka do Plaudu“ / „mail sobě s předmětem Hlasovka“ / „večerní check-in v Coworku“ (kombinace čárkou) | `CLAUDE.md`, `SKILL_MAP.md`, `JAK_MLUVIT_S_CLAUDEM.md` |
| `{{VSTUP_KDY}}` | G2 | `CLAUDE.md`, `JAK_MLUVIT_S_CLAUDEM.md` |
| `{{VODITKA}}` | G3, číslovaný seznam jeho slovy | `JAK_MLUVIT_S_CLAUDEM.md` |
| `{{BRIEF_CAS}}` | G4 | `CLAUDE.md`, `SKILL_MAP.md`, `JAK_MLUVIT_S_CLAUDEM.md`, `ULOHY.md` |
| `{{OTAZEK_MAX}}` | G5 (číslo) | `CLAUDE.md`, `JAK_MLUVIT_S_CLAUDEM.md`, `ULOHY.md` |
| `{{BEZ_VSTUPU}}` | G6 jeho slovy | `ULOHY.md` |
| `{{SCHUZKY_PRAVIDLO}}` | G7 (které schůzky zapisovat) | `SKILL_MAP.md`, `ULOHY.md` |
| `{{PREPISY_POSTUP}}` | G7 (odkud se berou přepisy online callů a jak se dostanou do vaultu; když nenahrává: „nenahrávám, píšu si poznámky“) | `SKILL_MAP.md` |
| `{{MAIL_ADRESA}}` | G1: přesná adresa, ze které i na kterou si posílá Hlasovku (bez mailu sobě: „(nepoužívám)“) | `ULOHY.md`, `JAK_MLUVIT_S_CLAUDEM.md` |
| `{{REVIEW_KDY}}` | G8 (když review nechce automaticky: „jen na slovo“) | `CLAUDE.md`, `SKILL_MAP.md`, `DASHBOARD.md`, `ULOHY.md` |
| `{{UDRZBA_KDY}}` | G8 (když ji nechce automaticky: „jen na slovo“) | `ULOHY.md` |
| `{{DIGEST_CAS}}` | G8 (když ho nechce automaticky: „jen na slovo“) | `ULOHY.md` |
| `{{DIGEST_TEMATA}}` | G8 (když digest nechce: „(zatím žádná)“) | `ULOHY.md` |
| `{{OBSAH}}` | H4: `ano` / `ne` | `ULOHY.md` (review, krok 8) |
| `{{NASTROJE}}` | H1 až H3, odrážky (nástroj, k čemu, konektor ano/ne) | `MI.md` |
| `{{CITLIVE}}` | J1 | `CLAUDE.md`, `VAULT_MAP.md`, `CLAUDE_RULES.md` |
| `{{ODDELENI_FIREM}}` | J2 | `CLAUDE.md`, `CLAUDE_RULES.md` |
| `{{OSOBNI}}` | J3 (co kromě deníku patří do `50-Osobni`) | `VAULT_MAP.md` |
| `{{FIREMNI_DATA}}` | otázka 03 jednou až dvěma větami (co se smí a nesmí zapisovat) | `CLAUDE.md`, `CLAUDE_RULES.md` |
| `{{TRENINK_DO}}` | ve fázi 2 text „(nastaví se ve fázi 4)“, ve fázi 4 den prvního zpracování + 14 dní | `SETUP.md`, `JAK_MLUVIT_S_CLAUDEM.md` |

Když něco v rozhovoru nezaznělo: `(doplnit)` + řádek do `SETUP.md` →
Otevřené. Prázdné sloupce Režim, Model a Založeno v tabulce Přehled
v `ULOHY.md` se doplní ve fázi 4 (nejsou to `{{…}}` místa).

## Pravidla psaní do vaultu

- Česky, stručně, fakticky. Časově citlivé vždy s datem.
- Nové soubory bez diakritiky a bez mezer v názvu.
- Datované záznamy `RRRR-MM-DD[-slug].md`, týdny `RRRR-Wxx.md`, měsíce `RRRR-MM.md`.
- Frontmatter mají věci se stavem (zakázka, kontakt, projekt, firma)
  a schůzky. Deníky bez něj.
- **Hodnoty frontmatteru malými písmeny a bez diakritiky** (`ja`, ne `já`),
  jinak je přehledy `.base` nenajdou.
- Wikilinky na všechno, co souvisí. Souvislosti jsou polovina hodnoty.
