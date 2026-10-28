# ChatGPT Work: co je jinak

Platí, když uživatel ve fázi 0 řekl, že druhý mozek poběží v **ChatGPT
Work** (v `SETUP.md` řádek `Appka: ChatGPT Work`). Celý zbytek skillu
platí stejně: rozhovor, vault, šablony, úlohy v `ULOHY.md`, trénink,
hranice. Tenhle soubor jen nahrazuje kroky, které jsou v Claude Coworku
jinak. **Kde se tenhle soubor a ostatní reference liší, platí tenhle.**

Rozhraní ChatGPT Work se rychle mění a tenhle postup ještě neprošel
testem u skutečného uživatele. Názvy tlačítek ber jako vodítko: když
nesedí, nech ho popsat, co vidí, a veď ho podle toho. Nikdy příkazy do
Terminálu. Co nejde udělat klikáním, zapiš do `SETUP.md` → Otevřené.

## Slovník: jak číst ostatní reference

| V referencích stojí | V ChatGPT Work to znamená |
|---|---|
| Claude (jako asistent) | ty, ChatGPT |
| Cowork, Cowork session | ChatGPT Work v desktopové appce ChatGPT |
| appka Claude, tarif Claude, účet Claude | appka, tarif a účet ChatGPT |
| Claude projekt, projekt Druhý mozek | projekt Druhý mozek v ChatGPT (část B) |
| konektor, adresář konektorů | plugin (aplikace) v katalogu pluginů (část C) |
| připojená složka | lokální složka, ke které má Work přístup (část A) |
| naplánovaná úloha, „Run now“ | naplánovaná úloha v desktopové appce ChatGPT (část D) |

## A. Předpoklady (místo fáze 0, krok 1, a `03_nastaveni.md` A3)

1. **Tarif a appka.** ChatGPT Work potřebuje placený tarif ChatGPT
   a **desktopovou appku ChatGPT** pro Mac nebo Windows. Dostupnost se
   liší podle tarifu a u firemního účtu podle nastavení správce. Ověř,
   že v desktopové appce Work vidí. Web ani telefon na soubory
   v počítači nedosáhnou, takže stavba i práce s vaultem jdou jen přes
   desktop.
2. **Obsidian a umístění vaultu** stejně jako v `03_nastaveni.md`,
   části A1 a A2.
3. **Přístup ke složce.** Ve Work otevřít složku `Vault` jako lokální
   složku (projekt) a povolit přístup **jen k ní**, ne k celému disku
   ani k domovské složce. Bez přístupu ke složce nejde nic zapsat.
   Do `SETUP.md` zapsat cestu, jak ji vidí počítač (`/Users/…/Vault`,
   `C:\Users\…\Vault`).
4. Když Work nabízí volbu mezi lokální prací a prací v cloudu, pro
   druhý mozek vždy **lokální**. Cloud na složku v počítači nedosáhne.

## B. Projekt Druhý mozek (místo `03_nastaveni.md` B)

1. V appce ChatGPT → Projekty → Nový projekt → název **Druhý mozek**.
   Když setup už v projektu běží, nový nezakládej. Na firemním účtu nech
   projekt soukromý.
2. Do instrukcí projektu vlož stejný text jako v `03_nastaveni.md`,
   část B, krok 3 (s doplněným `{{MENTOR_HLIDA}}`). Dej ho v bloku ke
   zkopírování.
3. **Od teď:** každá práce se vaultem = ChatGPT Work **v projektu Druhý
   mozek + přístup ke složce Vault.**
4. **Paměť ChatGPT** je pomocná, hlavní paměť je vault. Když nechce, aby
   se do paměti ChatGPT dostávaly citlivé věci z vaultu, ať u projektu
   zapne paměť jen pro projekt, nebo ji vypne (když to appka nabízí).
5. **`AGENTS.md` v kořeni vaultu** (zakládá se ve fázi 2): některé
   nástroje OpenAI čtou ve složce automaticky `AGENTS.md`. Ať najde
   cestu k pravidlům, i když instrukce projektu chybí:

```
# Instrukce pro asistenta

Pravidla pro práci s tímhle vaultem jsou v CLAUDE.md ve stejné složce. Na začátku každé práce si ho přečti celý a řiď se jím. Název souboru je historický, pravidla platí pro tebe stejně. Tenhle soubor neměň a nic dalšího do něj nepiš.
```

## C. Pluginy (místo `03_nastaveni.md` C)

Konektorům se v ChatGPT říká **pluginy** (nebo aplikace). Najde je
v appce pod Customize → Plugins (nebo v Nastavení), v konverzaci se na
ně odkazuje přes „@“. Připojit **před** založením naplánovaných úloh,
jen to, co reálně použije. Pravidlo o pracovních účtech na osobním
účtu (otázka 03) platí stejně.

- **Gmail / Outlook, Google Kalendář / Outlook, Google Drive:** stejný
  účel a stejné ověření jako v `03_nastaveni.md` C (Ověření po
  připojení).
- **Plaud: jen když ho v katalogu pluginů najde.** Když tam není,
  hlasovky přes Plaud ranní zpracování samo nepřečte. Pak doporuč jako
  denní vstup **mail sobě** nebo **check-in** (rozhovor, G1) a Plaud
  nech na schůzky s ručním exportem přepisu do `05-Inbox/Prepisy/`.
  Když plugin existuje, ověř, že vrátí seznam nahrávek a celý text
  přepisu (ne jen shrnutí). Názvy nástrojů v `ULOHY.md` (`list_files`,
  `get_transcript`) pak oprav na ty, které plugin skutečně má.
- **Oprávnění:** když plugin umožňuje omezit akce (jen čtení, zákaz
  odesílání a mazání), nastav to pro e-mail a kalendář. Když ne, zapiš
  do `SETUP.md` → Otevřené. Pravidla v `ULOHY.md` (konektory jen číst,
  nic neodesílat) platí tak jako tak.
- **Na firemním účtu** pluginy povoluje správce. Když plugin chybí, ať
  požádá správce.

## D. Naplánované úlohy (místo zakládání úloh v `04_ulohy.md`)

Princip ze `04_ulohy.md` platí beze změny: zadání žije v
`00-System/ULOHY.md`, prompt je stejný a o režimu (automaticky, nebo
na slovo „ráno“) rozhoduje test. Jinak je jen zakládání:

1. Úlohu zakládej **v desktopové appce**, ve Work u projektu se
   složkou `Vault`. Úloha založená na webu nebo v telefonu běží
   v cloudu a na složku v počítači nedosáhne.
2. Když appka nabízí, kde má úloha běžet, vyber **lokální projekt
   (složku Vault)**, ne kopii ani worktree.
3. Úloha běží bez dohledu s **výchozím nastavením sandboxu**. Musí smět
   číst a zapisovat ve složce `Vault`, víc ne. Když úloha hlásí, že
   zápis nepovolil sandbox, ukaž mu, kde v nastavení appky povolit
   zápis do projektové složky. Přístup k celému disku nedávej.
4. Prompt úlohy je stejný jako v `04_ulohy.md`.
5. Hned ji spusť ručně a zkontroluj `00-System/BRIEF.md` stejně jako
   v `04_ulohy.md` (Automatický, nebo ruční režim). Kontrola druhý den
   ráno ve fázi 5 platí stejně.
6. **Úlohy spouštěné událostí** (třeba „přišel mail“) nepoužívej. Běží
   na webu, ne v desktopové appce, takže na vault nedosáhnou.

Když nejde naplánovanou úlohu založit vůbec, je to **ruční režim**:
ráno ve Work v projektu Druhý mozek napíše „ráno“.

## E. Provoz (místo `03_nastaveni.md` D)

- Úloha, která zapisuje do vaultu, potřebuje **zapnutý počítač
  a spuštěnou desktopovou appku ChatGPT**. Ranní čas volit, kdy je
  počítač reálně otevřený. Notebook se zavřeným víkem neudrží vzhůru
  nic.
- Work spotřebuje víc než běžný chat. Když narazí na limity tarifu,
  digest a údržbu pouštět jen na slovo, ranní zpracování nechat.
- Plaud (když je přes plugin) přepisuje až po synchronizaci z telefonu.

## F. Přepis vaultu pro ChatGPT (fáze 2)

Šablony v `assets/vault/` mluví o Claudovi a Coworku. Ve fázi 2, při
vyplňování soubor po souboru, v textu **pro ChatGPT Work** přepiš:

| V šabloně | Napiš |
|---|---|
| Claude, Clauda, Claudovi, s Claudem… | ChatGPT (nesklonné: „s ChatGPT“, „pro ChatGPT“) |
| Cowork, v Coworku, Cowork session | ChatGPT Work, ve Work |
| appka Claude, tarif Claude, účet Claude | appka ChatGPT, tarif ChatGPT, účet ChatGPT |
| konektor | plugin (jen tam, kde jde o nastavení v appce) |

**Názvy souborů a wikilinky neměň** (`CLAUDE.md`, `CLAUDE_RULES.md`,
`JAK_MLUVIT_S_CLAUDEM.md`, `[[CLAUDE_RULES]]` …). Celý systém na ně
odkazuje. Kde je název souboru v textu, který uživatel čte, stačí ho
nechat; jednou větou mu ve fázi 2 řekni, že „CLAUDE“ v názvu je
historické.

Pak založ `AGENTS.md` v kořeni vaultu (text v části B, krok 5),
jen když ještě neexistuje.

**Kontrola na konci fáze 2** (vedle té ze `SKILL.md`): ve vaultu není
slovo „Claude“ ani „Cowork“ nikde kromě názvů souborů a wikilinků.
