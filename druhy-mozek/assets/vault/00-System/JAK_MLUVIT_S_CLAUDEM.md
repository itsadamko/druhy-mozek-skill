# Jak mluvit s Claudem (tahák)

*Založeno: {{DATUM}} • Trénink do {{TRENINK_DO}}, pak už jen tahák.
Workflow → [[SKILL_MAP]]*

## Proč to celé

Druhý mozek je tak dobrý, kolik se do něj denně dostane. Nejlevnější
cesta je pár minut mluvení: Claude z toho udělá zápisy k lidem, sliby
s termíny, posun zakázek a otázky na ráno.

## Denní vstup

**Jak:** {{VSTUP}}
**Kdy:** {{VSTUP_KDY}}. 2 až 5 minut stačí.

[POKUD PLAUD]
- **Plaud:** nahrát, nic dalšího. Přepis a zpracování proběhnou samy
  (přepis až po synchronizaci z telefonu nebo zařízení).
[/POKUD]
[POKUD MAIL]
- **Mail sobě:** nový mail z {{MAIL_ADRESA}} na tutéž adresu, předmět
  přesně **Hlasovka**, text nadiktovat (mikrofon na klávesnici
  telefonu), odeslat. Hotovo. Z jiné adresy ho ranní zpracování nenajde.
[/POKUD]
[POKUD CHECKIN]
- **Check-in:** v Coworku v projektu Druhý mozek napsat nebo nadiktovat
  (Mac: dvakrát Fn, Windows: Win + H) „check-in: …“. Claude to roztřídí
  hned a řekne kam.
[/POKUD]

**Vodítka:**

{{VODITKA}}

**Co z toho dělá data** (Claude se na to ráno doptá, když to chybí):

- **Celé jméno a firma** u lidí („Petr Novák z Alfy“, ne „Petr“)
- **U slibu kdo, co a do kdy** („do pátku pošlu…“)
- **Čeho se to týká** (která zakázka, projekt, firma)
- **Jak to dopadlo**, ne jen „nějak to dopadlo“
- **Kdo co udělá**, ne jen „domluvili jsme se“

Vzor:

> „Dneska jsem byl na obědě s Petrem Novákem z firmy Alfa. Slíbil jsem
> mu, že mu do pátku pošlu nabídku na školení. On mi slíbil, že do konce
> měsíce řekne, jestli jdou do pilotu. A seznámil jsem ho s Janou
> Svobodovou kvůli náboru.“

Z toho vznikne: zápis k Petrovi, dva sliby s termínem, propojení
Petr × Jana, zakázka u Alfy.

**Soukromé věci** můžu říct taky. Jdou jen do deníku, nikam jinam.

## Ráno

Ranní zpracování ({{BRIEF_CAS}}, automaticky, nebo když napíšu „ráno“)
roztřídí denní vstup a přepisy schůzek a napíše [[BRIEF]]: dnešní
schůzky, sliby, co čeká na mě a max. {{OTAZEK_MAX}} otázky. Na otázky
odpovím v dalším denním vstupu, nebo v Cowork session v projektu Druhý
mozek na počítači (vault leží na počítači, z telefonu se do něj
nezapíše).

**Můj ranní rituál** *(doplní se při setupu, fáze 5, klik po kliku)*:

1. (doplnit)
2. (doplnit)
3. (doplnit)

## Věty, které stojí za to znát

| Řeknu | Stane se |
|---|---|
| „Ráno“ | ranní zpracování a brief (když neběží samo); když už dnes proběhlo, jen ukáže brief |
| „Ráno znovu“ | zpracuje, co od rána přibylo, a přepíše brief |
| „Zpracuj starší“ | vstupy, které čekají (po dovolené, nad denní limit) |
| „Připrav mě na schůzku s X“ | karta, historie, otevřené sliby, stav zakázky |
| „Co víš o X?“ | rychlé shrnutí člověka, firmy nebo zakázky |
| „Zapiš: …“ (nebo nadiktuju cokoli) | Claude roztřídí do vaultu a řekne kam |
| „Check-in: …“ | večerní vstup, zpracuje se hned |
| „Odesláno“ | zápis odeslaného dokumentu k zakázce |
| „Kdo mi co dluží?“ / „Co jsem komu slíbil?“ | přehled slibů |
| „Koho jsem dlouho neviděl?“ | lidi k udržení |
| „Deník“ / „Týdenní review“ / „Měsíční review“ | rituály podle [[SKILL_MAP]] |
| „Tohle nedělej“ / „Takhle ne, ale takhle“ | nové pravidlo do [[CLAUDE_RULES]] |
| „Vyhodnoť trénink“ | vyhodnocení tréninku (níž) |

## Vyhodnocení tréninku (7. a 14. den, do {{TRENINK_DO}})

Na „vyhodnoť trénink“ Claude projde [[VSTUP_STAV]], deníky a briefy od
začátku tréninku a napíše do [[SETUP]] (fáze 6):
- kolik denních vstupů a schůzek, kolik z nich vzniklo slibů, lidí
  a zakázek
- co se ve vstupech zlepšilo a co pořád chybí
- jeden návrh úpravy (vodítka, čas briefu, počet otázek, cesta vstupu),
  nebo nic
- 14. den navíc moje slovo: drží to? Pak se trénink vypne.

## Co Claude nedělá

- Neposílá maily ani zprávy za mě bez výslovného pokynu.
- Nezapisuje do cizích systémů bez mého pokynu.
- Nevynáší citlivé věci.
- Nedomýšlí si, co jsem neřekl. Když neví, zeptá se.
