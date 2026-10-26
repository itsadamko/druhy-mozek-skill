# Druhý mozek

**Claude skill, který ti rozhovorem postaví vlastní druhý mozek v Claude Coworku.**

Obsidian vault s pravidly pro Clauda, osobní profil s rozhodovacím
filtrem, lidi a sliby, schůzky, zakázky a projekty. K tomu denní smyčka:
večer pár minut hlasovky nebo krátký zápis, ráno brief s tím, co tě dnes
čeká, a max. tři otázky na doplnění. Prvních 14 dní tě Claude učí, jak
s ním mluvit, aby z toho šla data.

Pro lidi, co pracují: zaměstnance, podnikatele, freelancery i kombinace.
Česky, bez programování a bez terminálu, všechno klikáním a mluvením.

> [!NOTE]
> Neoficiální osobní projekt. Není spojený s firmou Anthropic ani jí
> schválený.

---

## Co budeš potřebovat

- **Placený tarif Claude** (Pro, Max, Team nebo Enterprise). Cowork
  v bezplatném tarifu není.
- **Desktopovou appku Claude** pro Mac nebo Windows ([claude.com/download](https://claude.com/download)).
  Vault leží na tvém počítači, z prohlížeče ani z telefonu na něj Claude
  nedosáhne.
- **Obsidian** ([obsidian.md](https://obsidian.md), zdarma). Skill tě
  instalací provede.
- Volitelně **Plaud** na hlasovky a nahrávky schůzek. Bez něj to jde
  přes mail sám sobě nebo krátký večerní zápis.
- **Čas:** rozhovor 1 až 2 hodiny (klidně ve dvou sezeních), nastavení
  další hodina. Pak 14 dní tréninku po pár minutách denně.

## Instalace

1. Stáhni **[druhy-mozek.zip](https://github.com/itsadamko/druhy-mozek-skill/raw/main/druhy-mozek.zip)**
   (nerozbaluj ho).
2. V appce Claude otevři **Customize → Skills** (nebo Nastavení →
   Capabilities → Skills), dej **přidat / nahrát skill** a vyber
   stažený zip. Názvy tlačítek se mezi verzemi appky mění, hledej
   „Skills“.
3. V desktopové appce založ projekt **Druhý mozek**, spusť v něm
   **Cowork** a napiš: **„Nastav mi druhý mozek.“**
4. Claude se zeptá, jestli tykat, nebo vykat, a dál tě vede krok po
   kroku. Stav nastavení si ukládá do vaultu (`00-System/SETUP.md`), takže
   můžeš kdykoli přestat a příště napsat „Pokračuj v nastavení druhého
   mozku“.

## Co vznikne

```
Vault/
├── CLAUDE.md          ← jak s tebou má Claude pracovat (role, tón, pravidla)
├── 00-System/         ← tvůj profil a filtr (MI), pravidla, úlohy, ranní brief
├── 05-Inbox/          ← nezařazené, přepisy schůzek
├── 10-Firmy/          ← firmy, kde pracuješ nebo které vedeš
├── 15-Zakazky/        ← zakázky a obchod (když je máš)
├── 20-Lide/           ← lidi, sliby, propojení
├── 25-Schuzky/        ← zápisy ze schůzek
├── 30-Projekty/       ← projekty s cílem a koncem
├── 40-Znalosti/       ← know-how, rešerše
├── 50-Osobni/         ← deník (citlivé, nikam ven)
├── 60-Assets/         ← šablony
└── 90-Archiv/         ← hotové věci (nic se nemaže)
```

**Denní smyčka:**

- **Večer:** hlasovka do Plaudu, mail sám sobě s předmětem „Hlasovka“
  nadiktovaný v telefonu, nebo krátký „check-in“ v Coworku.
- **Ráno:** Claude vstup roztřídí (lidi, sliby, zakázky, deník) a napíše
  brief: dnešní schůzky, sliby po termínu, co čeká na tebe, max. tři
  otázky. Podle tarifu a verze appky to běží samo jako naplánovaná úloha,
  nebo napíšeš „ráno“ a stane se totéž. Skill to při nastavení vyzkouší.
- **Týdně (volitelně):** review, úklid vaultu, přehled novinek z oboru.

## Soukromí a firemní data

- Vault je **obyčejná složka s textovými soubory na tvém počítači.**
  Patří tobě a otevřeš ho i bez Clauda.
- Hned na začátku se skill zeptá, **jestli smíš pracovní informace dávat
  do svého Claude** (firemní pravidla pro AI). Podle odpovědi omezí, co
  se zapisuje. Na osobní účet Claude nepřipojuje pracovní mail ani
  kalendář bez souhlasu firmy.
- Ranní zpracování čte **jen** tvoje hlasovky (u mailu jen zprávy, které
  sis poslal sám s předmětem „Hlasovka“), nic jiného ve schránce.
- Claude za tebe nic neposílá, nic nemaže a hesla ani přístupy do vaultu
  nezapisuje.

## Obsah repa

- `druhy-mozek/`: zdroj skillu (`SKILL.md`, `references/` s postupy,
  `assets/vault/` se šablonami vaultu)
- `druhy-mozek.zip`: totéž zabalené k nahrání do Claude

## Licence

MIT, viz [LICENSE](LICENSE).
