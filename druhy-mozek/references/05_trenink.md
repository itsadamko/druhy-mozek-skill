# Trénink: dva týdny, než se z toho stane návyk

Proč: vault bez denního přísunu je archiv. Každý, kdo s druhým mozkem
začíná, řeší totéž: naučit se s Claudem mluvit tak, aby z toho šla data,
a dělat to denně. Trénink trvá 14 dní od stavby vaultu (datum konce je
v `SETUP.md`).

Vyhodnocení po 7 a 14 dnech spouští uživatel větou „vyhodnoť trénink“
(ranní brief mu ji ten den připomene), nebo ho udělá týdenní review,
když běží. Postup je v `00-System/JAK_MLUVIT_S_CLAUDEM.md`.

## Co dělá Claude v tréninku

**Každé ráno (ranní zpracování, sekce Trénink v briefu):**
- Jedna věta, **co ve vstupu chybělo**, aby z něj byla data. Typicky:
  - u slibu chybělo **do kdy**
  - u člověka chybělo **příjmení nebo firma** (nejde spárovat s kartou)
  - nebylo jasné, **které zakázky nebo projektu** se věc týká
  - zaznělo „nějak to dopadlo“ bez **výsledku**
  - zaznělo „domluvili jsme se“ bez toho, **kdo co udělá**
- Jedna věta, **co bylo dobře** (konkrétně, ne „super“).
- Nikdy víc než dvě věty. Žádné hodnocení délky ani stylu mluvy.

**Když vstup nepřišel:** podle volby z rozhovoru (G6). Výchozí: jedna
věta a dvě rychlé otázky místo vstupu. Nepočítat dny, nevyčítat.

**Po 7 dnech** (týdenní review, sekce Trénink, nebo „vyhodnoť trénink“):
- kolik vstupů, kolik schůzek, kolik slibů a lidí z nich vzniklo
- co se zlepšilo, co pořád chybí
- návrh jedné úpravy: vodítka, čas briefu, počet otázek, cesta vstupu
  (třeba přechod z check-inu na mail sobě), nebo nic

**Po 14 dnech:**
- stejné vyhodnocení jako po 7 dnech + verdikt uživatele: drží to?
- vypnout sekci Trénink (stačí, že datum v `SETUP.md` uplynulo)
- odškrtnout fázi 6 v `SETUP.md`
- nové pravidlo z jeho korekcí zapsat do `CLAUDE_RULES.md` část B

## Zkušební vstup: co ukázat při setupu

Zkušební vstup udělá ve fázi 4 (2 minuty, podle vodítek). Claude ho
zpracuje a ukáže, co z něj vzniklo: zápis do deníku, slib v kartě
člověka, otázka v briefu. **Tohle je okamžik, kdy pochopí, proč to dělá.**
Bez něj je denní vstup další povinnost.

Příklad dobré věty (dát mu ho jako vzor, upravený na jeho práci):

> „Dneska jsem byl na obědě s Petrem Novákem z firmy Alfa. Slíbil jsem
> mu, že mu do pátku pošlu nabídku na školení. On mi slíbil, že do konce
> měsíce řekne, jestli jdou do pilotu. A seznámil jsem ho s Janou
> Svobodovou kvůli náboru.“

Z jedné věty vznikne: zápis k Petrovi, dva sliby s termínem, propojení
Petr × Jana, zakázka u Alfy. To je celé kouzlo.

Pro zaměstnance bez obchodu stejný princip, a jen v mezích, které
zazněly v otázce 03 o firemních datech: „Šéfová Eva Malá chce do středy
report. Slíbil jsem kolegovi Tomášovi Bartošovi, že mu zítra pošlu
podklady. Chci se do konce měsíce přihlásit na kurz vyjednávání.“

## Další návyky, které stojí za to ukázat (v tréninku, ne najednou)

- **„Připrav mě na schůzku s X“** → Claude vytáhne kartu, historii,
  sliby a poslední zápis (den 2 až 3, před reálnou schůzkou).
- **„Co víš o X?“** → rychlý dotaz v Coworku na počítači.
- **„Co jsem komu slíbil?“ / „Kdo mi co dluží?“** → přehled slibů.
- **„Zapiš: …“** → cokoli během dne, Claude roztřídí.
- **„Odesláno“** u dokumentu → zápis do zakázky (když posílá nabídky).
- **„Týdenní review“** → když ho nechce automaticky.

Jeden nový návyk za pár dní, ne všechno první den.
