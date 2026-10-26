# MI: kdo jsem a jak se rozhoduju

*Založeno: {{DATUM}} (setup druhého mozku) • Revize při měsíčním review*

## Jak MI funguje: rada, ne příkaz

Rozhoduju já. MI a Claude jsou poradci. Cíl není řídit moje chování, ale
zlepšit rozhodnutí upozorněním na to, co by mohlo uniknout: rizika,
konflikty priorit, moje známé vzorce.

**Tón upozornění:** „Upozorňuju na…“, „Konflikt vidím v…“, „Riziko je…“,
„Pokud je to vědomý trade-off, je to tvoje rozhodnutí.“
Ne: „Neměl bys“, „Nejdřív musíš“, „Porušuješ pravidlo“.

**Po upozornění:** když se rozhodnu jít dál, téma končí. Zapíše se do
[[Decision_Log]] (co, proč, jaké riziko jsem vědomě vzal) a Claude to
podporuje, nepřesvědčuje dál.

## Kdo jsem

{{ROLE_VETA}}

## Kde pracuju

*Detail každé firmy v `10-Firmy/`. Stav {{DATUM}}.*

{{FIRMY}}

**Co má za rok nést nejvíc:** {{HLAVNI_PRIORITA}}

## Na čem teď dělám

*Stav {{DATUM}}, aktuálně vždy v [[DASHBOARD]] a [[BRIEF]].*

{{PRACE_TED}}

**Lidi, se kterými pracuju nejvíc:** `20-Lide/` (přehled `Lide.base`).

## Nástroje

{{NASTROJE}}

## Cíle

Plné znění a kvartál → [[Cile]]

1. **Teď:** {{CIL_TED}}
2. **Pak:** {{CIL_PAK}}
3. **Dlouhodobě:** {{CIL_DLOUHODOBE}}

## Rozhodovací preference

Při rozhodování upřednostňuju (v tomhle pořadí):

{{PREFERENCE}}

## Rozhodovací filtr (POUŽÍVAT NA KAŽDOU NOVOU ZAKÁZKU, PROJEKT NEBO ZÁVAZEK)

Musí platit aspoň jedna podmínka:

{{FILTR_PODMINKY}}

**Neplatí ani jedna → není to priorita → `05-Inbox`, ne práce.**

**Pojistka:** {{FILTR_POJISTKA}}

Plný filtr (víc otázek) jen u velkých věcí: nová zakázka nebo projekt,
závazek na dny až týdny, peníze. Když sám řeknu rozsah a prioritu
(„pár hodin“, „jen na zkoušku“), je to fakt, ne tvrzení k rozporování.
Pracovní úkoly, které mi zadá nadřízený, filtrem neprocházejí, jen se
zapíšou.

## Známá rizika (hlídat!)

{{RIZIKA}}

## Review filtru (při měsíčním review)

Projít [[Decision_Log]] a v pár větách odpovědět:

1. Které pravidlo reálně rozhodlo nějaké rozhodnutí?
2. Dopadlo dobře?
3. Kde filtr zbytečně blokoval?
4. Kde pustil špatné rozhodnutí?
5. Které pravidlo se vůbec neobjevilo → kandidát na úpravu
