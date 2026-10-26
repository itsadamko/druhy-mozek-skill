# SKILL_MAP: jak se s vaultem pracuje

*Založeno: {{DATUM}} • Workflow pro mě i pro Clauda. Struktura: [[VAULT_MAP]]*

## 1. Denní vstup

Můj denní vstup: **{{VSTUP}}**, podle vodítek v [[JAK_MLUVIT_S_CLAUDEM]].
Ráno ({{BRIEF_CAS}}) ho zpracuje ranní zpracování ([[ULOHY]], sekce 1).
Stejně se zpracuje cokoli, co nadiktuju nebo napíšu v session.

[POKUD PLAUD]
- **Plaud:** nahraju hlasovku, Plaud ji přepíše, ranní zpracování si ji
  přečte přes konektor samo.
[/POKUD]
[POKUD MAIL]
- **Mail sobě:** v telefonu nadiktuju mail sám sobě s předmětem přesně
  „Hlasovka“. Ranní zpracování čte jen tyhle maily, žádné jiné.
[/POKUD]
[POKUD CHECKIN]
- **Večerní check-in:** v Cowork session v projektu Druhý mozek napíšu
  nebo nadiktuju „check-in: …“. Claude to hned roztřídí (body níž)
  a zapíše do deníku dne (`50-Osobni/Denik/RRRR-MM-DD.md`, formát
  z [[ULOHY]] sekce 1, krok 3; když deník existuje, jen doplní sekci
  `## Z denního vstupu`). Pak řádek do [[VSTUP_STAV]] (zdroj `session`,
  typ `checkin`), ať ho ranní zpracování nebere znovu. V tréninku hned
  jedna věta, co chybělo, a jedna, co bylo dobře.
[/POKUD]

Claude třídí sám, neptá se „kam to dát“:
1. **Novinka k člověku** → `20-Lide/<Jmeno>.md`: Historie + `posledni_kontakt`
2. **Slib** (můj nebo mně) → řádek slibu (workflow 3)
3. **Propojení lidí** → workflow 4
4. **Zakázka nebo obchod** → `15-Zakazky/` (workflow 5). Nová
   příležitost, o které se rozhoduju → navíc otázka s verdiktem filtru
   z [[MI]]
5. **Projekt** → `30-Projekty/` Log, frontmatter (`ceka_na`, `termin`, `dalsi_krok`)
6. **Firma** (změna, rozhodnutí, partner) → `10-Firmy/<firma>.md` Historie
7. **Rozhodnutí** → deník; do [[Decision_Log]] jen když ho sám nazvu
   rozhodnutím
8. **Osobní věc** → jen deník
9. **Nejasné** → otázka do briefu, nedomýšlet

## 2. Schůzky a přepisy

1. Zápis → `25-Schuzky/Schuzka_<Kdo>_RRRR-MM-DD.md` ze šablony `Schuzka`,
   s polem `firma`.
2. **Přepis, ne shrnutí.** U nahrávek se čte celý přepis, ne jen AI
   shrnutí (shrnutí umí přisoudit čísla někomu jinému). **Čísla, částky
   a citace vždy z přepisu.** Stejná věc ze schůzky i z denního vstupu se
   zapisuje jednou (druhý zdroj se jen připíše).
3. Odkud přepisy beru: {{PREPISY_POSTUP}}
4. Které schůzky se zapisují: {{SCHUZKY_PRAVIDLO}}
5. Rozhodnutí a úkoly propsat: lidi (Historie), sliby, zakázka, projekt.
6. Co nezaznělo, se nedomýšlí. Patří do Otevřených otázek.
7. **Přepis vložený přímo do session** zpracuj hned a zapiš řádek do
   [[VSTUP_STAV]] (zdroj `session`).

**Složka `05-Inbox/Prepisy/`:** přepis (text, `.md`, `.txt`, `.docx`)
sem uložím. Ranní zpracování ho vezme a zapíše do [[VSTUP_STAV]]. Soubor
zůstává ve složce, dokud ho při review neodsouhlasím do `90-Archiv/`.
Stejná schůzka z víc zdrojů (Plaud i soubor) = jeden zápis.

**„Připrav mě na schůzku s X“:** karta člověka, poslední zápisy, otevřené
sliby oběma směry, propojení, stav zakázky. Max 10 řádků.

## 3. Sliby

1. Formát řádku a kde žije: [[VAULT_MAP]], sekce Řádky slibů. Slib
   konkrétnímu člověku → u člověka; slib klientovi bez jména → u zakázky;
   jinak u projektu nebo firmy. Člověk bez karty nebo nejasně komu →
   `05-Inbox/Sliby_k_zarazeni.md` + otázka do briefu
2. Každý slib má **kdo → komu, co, do kdy**. Bez data se doptat (brief)
3. Splněno → zaškrtnout + `✓ RRRR-MM-DD`
4. Ranní brief ukazuje sliby dnes a po termínu, týdenní review všechny
   po termínu

## 4. Lidé a propojení

1. Klíčový člověk → `20-Lide/Jmeno_Prijmeni.md` ze šablony `Kontakt`
2. U každého: kdo to je, firma a role, odkud se známe, čím může pomoct /
   čím můžu já, `udrzovat: ano/ne`
3. Po každém kontaktu: Historie + `posledni_kontakt`
4. **Propojení** (seznámím A s B): řádek do sekce `## Propojení` u obou
   (`RRRR-MM-DD · s kým · proč · výsledek: ?`). Po 30 dnech se týdenní
   review zeptá na výsledek
5. Lidi s `udrzovat: ano` a posledním kontaktem nad {{UDRZOVAT_DNI}} dní
   připomene týdenní review (max 3)
6. Osobní údaje třetích lidí (rodná čísla, zdravotní stav, životopisy,
   mzdy) do vaultu nevkládat, jen kde leží

## 5. Zakázky a obchod

**Pravda o zakázce žije ve frontmatteru jejího souboru.** Přehled je
`Zakazky.base`, ne ruční tabulka. Kde se obchod vede: {{KDE_OBCHOD}}

1. Nová zakázka → `15-Zakazky/Zakazka_<Klient>_<Nazev>.md` ze šablony
   `Zakazka`
2. Po **každém** kontaktu: `## Historie` + `posledni_kontakt` + `ceka_na` /
   `termin` / `dalsi_krok`
3. `ceka_na: ja` **musí** mít `termin`
4. Hotovo / prohráno → `stav`, poznatek do `## Poznatky pro příště`
   a do `40-Znalosti`, soubor do `90-Archiv` (po potvrzení)
5. Pole `vede_se`: `vault` (pravda je tady, stav ve frontmatteru) nebo
   `crm` (zakázka žije v systému, kde pracují i jiní; tady jen moje
   poznámky, Historie, sliby a odkaz, stavová pole se nevyplňují).
[POKUD VIC]
6. Firmy se nemíchají: ceny, klienti a lidi jedné firmy nejdou do
   výstupů jiné bez mého pokynu.
[/POKUD]

## 6. Dokumenty pro klienty

1. Název vždy s datem nebo verzí (`Nabidka_Klient_RRRR-MM-DD.pdf`, druhá
   verze `_v2`). Odeslaný soubor se nepřepisuje ani nepřejmenovává.
2. **Na moje „odesláno“** Claude zapíše do zakázky řádek do tabulky
   Odeslané dokumenty (dokument, verze, datum, komu) a do Historie.
3. **Odeslaný dokument = to, s čím počítá klient.** Když se vault
   a odeslaný dokument rozejdou, v hovoru s klientem platí odeslaný.

## 7. Znalosti a rešerše

1. „Nastuduj X“ → poznámka do `40-Znalosti/` (`Tema_RRRR-MM-DD.md`):
   co to je, co umí, kde jsou limity, zdroje s datem
2. Rešerše je znalost, ne návrh projektu. Filtr z [[MI]] až ve chvíli,
   kdy to chci použít nebo koupit
3. Tvrzení odstupňovat podle ověření (dva nezávislé zdroje / jeden
   zdroj / odhad)

## 8. Projekty a nové závazky

1. Pracovní projekt (zadaný v práci) → `30-Projekty/` ze šablony
   `Projekt`, bez filtru
2. Vlastní nový projekt nebo závazek → nejdřív filtr z [[MI]].
   Neprojde → `05-Inbox`, ne práce. Rozhoduju já.
3. Nová zakázka: zapsat poptávku do `15-Zakazky/` smí Claude hned
   (evidence není závazek). Filtr z [[MI]] přichází ve chvíli, kdy se
   rozhoduju, jestli řeknu ano.
4. Projekt bez pohybu přes 10 dní, zatímco běží jiný → řeší se v review

## 9. Týdenní review (trigger „týdenní review“, {{REVIEW_KDY}})

Postup v [[ULOHY]], sekce 2. Výstup `50-Osobni/Denik/RRRR-Wxx.md` ze
šablony [[Tydenni_Review]] a přepsaný [[DASHBOARD]].

## 10. Opakované procesy

{{VLASTNI_PROCES}}

## 11. Deník a měsíční review

- **Deník** (trigger „deník“): `50-Osobni/Denik/RRRR-MM-DD.md`.
  Za včerejšek ho ráno předpřipraví ranní zpracování. Já doplním jen to,
  co chci. Než Claude řekne, že zápis chybí, ověří to výpisem složky,
  ne z paměti.
- **Měsíční review** (trigger „měsíční review“): `50-Osobni/Denik/RRRR-MM.md`,
  co se povedlo a proč, vyhodnotit [[Cile]], projít [[Decision_Log]]
  a podle toho upravit filtr v [[MI]].
