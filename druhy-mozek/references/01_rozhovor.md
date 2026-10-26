# Rozhovor: otázky, doporučené odpovědi, kam to patří

## Metoda

- Jedna otázka najednou, ke každé doporučená odpověď. Formát:
  > **Otázka.** Návrh: „…“. Sedí, nebo jinak?
- O uživateli předem nic nevíš. Doporučené odpovědi jsou typické
  odpovědi lidí v jeho situaci, ne fakt o něm. Jakmile něco řekne,
  stav další návrhy na tom.
- **Grilování:** na vágní odpověď se doptej na konkrétní příklad
  z posledních dvou týdnů („kdy naposledy se ti to stalo?“, „u koho?“,
  „co přesně jsi udělal?“). Max dvě doptávací otázky, pak ulož jako
  otevřené.
- Když odpoví víc najednou, zapiš všechno a přeskoč, co už je zodpovězené.
- Po každé odpovědi checkpoint do `05-Inbox/RRRR-MM-DD-setup-rozhovor.md`.
- Pořadí drž, závislosti jdou shora dolů (profil → práce → lidé → cíle →
  filtr → smyčka → nástroje). Po bloku E nabídni pauzu.
- **U každé otázky je napsané, pro koho je.** Bez poznámky = pro všechny.
  Profil se určí v bloku 0:
  - **Z** = zaměstnanec (jedna firma, nadřízený, tým)
  - **P** = podnikatel nebo jednatel (jedna nebo víc firem)
  - **F** = freelancer, OSVČ (klienti a zakázky)
  - **VÍC** = má víc firem nebo rolí naráz (platí vedle Z, P, F)
  - **OBCHOD** = prodává, vede zakázky nebo obchodní vztahy s klienty

## Otázky

### 0. Profil (rozhoduje o rozsahu)

**01. Co z toho jsi? Klidně víc naráz.**
Nabídni: zaměstnanec / podnikatel nebo jednatel / freelancer (OSVČ) /
kombinace (třeba zaměstnání plus vlastní firma). Doptej se: kolik firem
nebo rolí paralelně, a jestli prodáváš nebo vedeš zakázky pro klienty.
→ urči profil (Z / P / F, VÍC, OBCHOD) a zapiš ho do souhrnu rozhovoru

**02. Co od druhého mozku čekáš nejvíc?**
Nabídni k výběru (víc možností): nezapomínat sliby a follow-upy / mít
přehled o lidech a vztazích / vědět, co se kde děje u zakázek / držet
fokus a nerozjíždět moc věcí / mít kde ukládat znalosti / mít deník a
odstup od práce.
→ pořadí důrazu v `CLAUDE.md` (Mentor) a v briefu

**03. Firemní data: smíš pracovní informace dávat do svého Claude?**
(Z povinně, ostatní když pracují s daty klientů nebo na cizím počítači.)
**Polož hned tady, ještě před jmény a projekty.** Doptej se: je tenhle
počítač firemní? Je účet Claude osobní, nebo firemní? Má firma pravidla
pro AI nástroje? Možnosti:
- **Firemní účet Claude a firma to povoluje** → bez omezení, jen citlivé
  podle J1.
- **Osobní účet, firma to povoluje nebo neřeší** → do vaultu moje
  poznámky; bez osobních údajů klientů a interních čísel, které by
  nesměly ven.
- **Nevím** → doporuč zjistit. Do té doby: kolegové jen jménem a rolí,
  bez hodnocení lidí, žádná interní čísla, termíny ani osobní údaje
  klientů. Zapsat do `SETUP.md` → Otevřené.
- **Firma to zakazuje** → druhý mozek jen na vlastní věci (osobní rozvoj,
  vlastní podnikání, kariéra, vlastní úkoly bez obsahu firmy), nebo setup
  odložit, až bude firemní účet. Řekni to na rovinu.
- **Firemní počítač a osobní účet** → zmínit, že instalace Obsidianu
  a záloh může narazit na pravidla IT.
**Od této chvíle se podle odpovědi řídí i soubor rozhovoru.**
→ `{{FIREMNI_DATA}}`: `CLAUDE.md`, `CLAUDE_RULES.md`; omezuje B1, A2, A3,
H1, H2

**04. Účty a zálohy.** *(výchozí)* Na jakém účtu Claude to poběží
(osobní, firemní) a kam se bude vault zálohovat? Návrh: „Všechno osobní,
ať to zůstane moje, i když změním práci.“ U „firma zakazuje / nevím“
z 03 zálohu firemních věcí na osobní disk nedoporučuj.
→ `SETUP.md`, fáze 3 (zálohy)

### A. Práce a role

**A1. Kdo jsi pracovně, jednou větou?**
Návrh podle profilu, třeba: „Vedu obchod ve firmě X a mám tým tří lidí.“
/ „Mám vlastní firmu na Y a k tomu dělám poradenství.“
→ `MI.md` Kdo jsem, `CLAUDE.md` úvod (`{{ROLE_VETA}}`)

**A2. Kde všude pracuješ a co tam děláš?**
U každé firmy nebo role: co dělá, tvoje role, zhruba kolik tvého času
(procenta stačí), s kým to děláš, kde se vede obchod a účetnictví (P, F).
U zaměstnance: firma, oddělení, nadřízený, tým.
→ `10-Firmy/<firma>.md` (šablona Firma), `MI.md` Kde pracuju (`{{FIRMY}}`)

**A3. Na čem teď nejvíc pracuješ? Top 3 až 5 věcí.**
→ `DASHBOARD.md`, `MI.md` (`{{PRACE_TED}}`), zakládá se z toho
`15-Zakazky/` a `30-Projekty/`

**A4. Je něco, co děláš pořád dokola stejně?** (týdenní report, nábor,
příprava nabídky, uzávěrka…)
Griluj krok po kroku: kdo co dělá, co padá mezi prsty. Jen opakované
procesy, ne jednorázové věci. Když žádný není, jdi dál.
→ `SKILL_MAP.md` workflow 10 (`{{VLASTNI_PROCES}}`), u firmy sekce
Opakované procesy

### B. Lidé

**B1. Kdo jsou nejdůležitější lidi kolem tebe?** (10 až 20 jmen)
Nadřízený a tým (Z), partneři a společníci (P), klíčoví klienti (F,
OBCHOD), lidi, se kterými se chceš potkávat. Ke každému jednou větou kdo
to je a jak se znáte. Celé jméno a firma.
→ `20-Lide/` (šablona Kontakt), u každého `udrzovat: ano/ne`

**B2. Sliby: co tě pálí víc, co slíbíš ty, nebo co slíbí tobě?**
Návrh: „Obojí. Ranní brief ukáže, co je dnes a co je po termínu.“
→ `SKILL_MAP.md` workflow 3, Ranní zpracování

**B3. Připomínat lidi, se kterými jsi dlouho nemluvil?** *(výchozí)*
Návrh: „Ano, v týdenním review max. 3 jména, jen u lidí s `udrzovat:
ano` a posledním kontaktem nad 60 dní.“ Ať řekne vlastní hranici.
→ `{{UDRZOVAT_DNI}}`

**B4. Propojuješ lidi mezi sebou?** (P, VÍC, OBCHOD; ostatním jen když
to sami zmíní)
Návrh: „Když někoho s někým seznámím, zapsat u obou kdo, koho, kdy
a proč, a za 30 dní se zeptat, co z toho vzniklo.“
→ `SKILL_MAP.md` workflow 4, šablona Kontakt (sekce Propojení)

### C. Zakázky a obchod (OBCHOD, F, P; zaměstnanci bez obchodu přeskočit)

**C1. Kde dnes vedeš zakázky a obchod?**
Rozliš tři případy:
- **Nikde pořádně** (hlava, mail) → od teď ve vaultu v `15-Zakazky/`.
- **Vlastní tabulka** (Excel, Google Sheets, poznámky), kterou vede jen
  on → nabídni jednorázový převod do `15-Zakazky/` (ať tabulku uloží do
  `05-Inbox/`, ve fázi 2 z ní založíš zakázky) a dál se vede ve vaultu.
  Tabulku pak nemusí udržovat.
- **Systém, ve kterém pracují i jiní** (CRM, firemní systém: Pipedrive,
  HubSpot, Raynet…) → pravda o stavu je tam, **vault ho nekopíruje**.
  Zakázky ve vaultu jen ty, ke kterým si chce vést vlastní poznámky,
  s `vede_se: crm`.
→ `10-Firmy/`, `VAULT_MAP.md`, `SKILL_MAP.md` workflow 5
(`{{KDE_OBCHOD}}`), pole `vede_se` v zakázkách

**C2. Kdo rozhoduje o ceně a podepisuje smlouvy?**
Návrh: „Já.“ U zaměstnance: „Nadřízený, já připravuju.“
→ `CLAUDE_RULES.md` Obchod (`{{CENA_SMLOUVY}}`)

**C3. Co chceš o zakázkách vidět ráno a co jednou týdně?**
Návrh: „Ráno: co čeká na mě dnes a co je po termínu. Týdně: co stojí přes
10 dní, co se posunulo, kde čekám já.“
→ Ranní zpracování a Týdenní review v `ULOHY.md`

### D. Cíle

**D1. Co chceš mít za 3 měsíce (teď), za rok (pak) a dlouhodobě?**
Pracovně i osobně, pokud chce. U „teď“ chtěj něco měřitelného (peníze,
povýšení, počet klientů, dokončený projekt, víc volna).
→ `Cile.md`, `MI.md` Cíle

**D2. Co má za rok nést nejvíc?** (VÍC: která firma nebo role; ostatní:
které téma nebo dovednost)
Pomáhá filtru rozhodovat, kam dávat čas.
→ `MI.md` (`{{HLAVNI_PRIORITA}}`), `Cile.md`

### E. Jak se rozhoduješ

**E1. Seřaď, co je pro tebe při rozhodování nejdůležitější.**
Nabídni k seřazení (může přidat vlastní): peníze, lidi a vztahy, smysl
a radost z práce, svoboda, rychlost, kvalita, jednoduchost, jistota,
čas pro sebe a rodinu.
→ `MI.md` Rozhodovací preference

**E2. Jaký vzorec tě nejvíc brzdí?**
Nabídni příklady, nic nepodsouvej: beru moc věcí naráz, slíbím
a zapomenu follow-up, všechno stojí na mně a nedeleguju, rozjíždím nové
věci rychleji, než dotahuju staré, nechám si rozšiřovat zadání, odkládám
nepříjemné, neumím říct ne. Griluj na příklad.
→ `MI.md` Známá rizika, `CLAUDE.md` Mentor

**E3. Kdy říct ano nové věci (zakázce, projektu, závazku, nápadu)?**
Z D1, D2 a E2 navrhni 3 až 5 podmínek, z nichž musí platit aspoň jedna,
plus jednu pojistku proti E2 (např. „max. N rozjetých nových věcí naráz“
nebo „nový závazek jen když vím, co kvůli němu odložím“).
→ `MI.md` Rozhodovací filtr

*Tady nabídni pauzu. Stav je v souboru rozhovoru, příště se navazuje.*

### F. Jak má Claude pracovat

**F1. Jaký tón chceš?** Nabídni:
1. **Věcný parťák:** přímý, klidný, bez omáčky
2. **Kouč:** víc se ptá, než radí
3. **Suchá ironie:** přátelské popichování, jako kamarád, co tě zná
4. Vlastní popis
Upřímnost má vždy přednost před vtipem.
→ `CLAUDE.md` Tón

**F2. Co ti má Claude jako mentor hlídat?**
Návrh: „Vzorec z E2, sliby a follow-upy, a že nová věc projde filtrem.“
→ `CLAUDE.md` Mentor, instrukce projektu (`{{MENTOR_HLIDA}}`)

**F3. Technika: Mac, nebo Windows? Telefon iPhone, nebo Android?**
Řekni mu na rovinu: **vault leží na počítači**, takže zápisy, odpovědi na
brief a dotazy do vaultu jdou v Cowork session na počítači. Z telefonu
jde denní vstup (hlasovka, mail sobě), ne práce s vaultem.
→ `CLAUDE.md` Práce s vaultem (`{{TECHNIKA}}`)

### G. Denní smyčka (to nejdůležitější)

Vysvětli jednou větou proč: „Vault bez denního přísunu je archiv.
Pár minut denně je rozdíl mezi archivem a druhým mozkem.“

**G1. Jak ti nejlíp půjde denní vstup?** Nabídni tři cesty:
1. **Plaud** (když ho má nebo chce): nahraje hlasovku, Plaud ji přepíše,
   ranní zpracování si ji přečte přes konektor samo. Nejpohodlnější,
   zvlášť když nahrává i schůzky.
2. **Mail sobě:** v telefonu nadiktuje mail sám sobě s předmětem
   „Hlasovka“ (diktování na klávesnici). Ranní zpracování ho přečte přes
   konektor e-mailu (Gmail, nebo Outlook, když v adresáři konektorů je).
   Funguje bez dalšího zařízení. **Doptej se, z jakého účtu telefon mail
   odesílá** (výchozí účet v Mailu / Gmailu) a zapiš přesnou adresu.
   Musí to být schránka, ke které jde připojit konektor, a podle 03 ne
   pracovní na osobním účtu Claude. Poskytovatel bez konektoru (Seznam,
   iCloud…) → nabídni check-in, nebo Gmail jen na tohle.
3. **Večerní check-in v Coworku:** 3 až 5 minut na počítači, napíše nebo
   nadiktuje do session v projektu „check-in: …“ a Claude to hned
   roztřídí. Nejjednodušší, ale potřebuje počítač.
Kombinace jde (třeba Plaud na schůzky a mail sobě na den).
→ `{{VSTUP}}`, `{{MAIL_ADRESA}}` a bloky `[POKUD PLAUD/MAIL/CHECKIN]`:
`CLAUDE.md`, `SKILL_MAP.md` workflow 1, `JAK_MLUVIT_S_CLAUDEM.md`,
`ULOHY.md`

**G2. Kdy a kde to reálně uděláš?**
Návrh: „Večer cestou domů, nebo po práci, 2 až 5 minut.“ Doptej se na dny,
kdy to nepůjde (ty vynechá, žádný problém).
→ `{{VSTUP_KDY}}`

**G3. Vodítka.**
Návrh tří:
1. Co je nového (lidi, práce, zakázky)
2. Co jsem komu slíbil a kdo mně, do kdy
3. Co řeším nebo rozhoduju
Chce přidat čtvrté (třeba „co mě dneska naštvalo nebo potěšilo“)?
Vodítka napiš jeho slovy, ať se mu dobře pamatují.
→ `{{VODITKA}}`: `JAK_MLUVIT_S_CLAUDEM.md` (ranní zpracování ho odtud čte)

**G4. Ranní brief: v kolik a kde ho chceš číst?**
Návrh: „8:00, soubor `00-System/BRIEF.md` v Obsidianu a krátce v Coworku.“
Čas volit, kdy je počítač reálně zapnutý. Řekni dopředu na rovinu:
jestli poběží sám (automaticky), nebo na slovo „ráno“, ukáže test ve
fázi 4. Celý brief je v Obsidianu na počítači; zkrácený výsledek
automatické úlohy jde obvykle vidět i v Claude appce v telefonu.
→ `{{BRIEF_CAS}}`

**G5. Kolik doplňujících otázek denně a jak na ně odpovíš?** *(výchozí)*
Návrh: „Max. tři. Odpovím v dalším denním vstupu, nebo v Cowork session.“
→ `{{OTAZEK_MAX}}`

**G6. Když denní vstup nepřijde, co má Claude ráno udělat?** *(výchozí)*
Návrh: „Jednou větou zmínit, že včerejšek chybí, a místo toho položit
dvě rychlé otázky. Žádné výčitky ani počítání dní.“ Když chce víc tlačit,
zapsat jeho slovy.
→ `{{BEZ_VSTUPU}}`

**G7. Schůzky: nahráváš je, nebo si píšeš poznámky?**
Osobní schůzky (Plaud, diktafon), online cally (přepis z Teams, Zoomu,
Google Meet, Plaud desktop…), nebo nic. Kdy nenahrává (citlivé jednání,
souhlas druhé strany)? Zápis z každé, nebo jen pracovní nad 15 minut?
Návrh: „Z každé pracovní. Soukromé přeskočit.“ Přepisy, které nejdou
přes konektor, stačí uložit do `05-Inbox/Prepisy/` (nebo vložit do
session) a ranní zpracování je vezme. Nahrávání jen se souhlasem druhé
strany; podle 03 nic, co by nesmělo ven.
→ `{{SCHUZKY_PRAVIDLO}}`, `{{PREPISY_POSTUP}}` (když nenahrává:
„nenahrávám, píšu si poznámky“): `SKILL_MAP.md` workflow 2, Ranní
zpracování

**G8. Které další úlohy chceš?**
Nabídni, ke každé návrh času:
- **Týdenní review:** návrh „pátek 15:00, ať je víkend volný“
- **Údržba vaultu** (jen hlásí nepořádek): návrh „pondělí ráno“
- **Ranní digest novinek** z oboru: návrh „ano, 7:30“ nebo „ne“; témata
  se doptej (obor, trh, nástroje, regulace)
Review je dobré mít i kvůli tréninku (vyhodnocení po 7 dnech).
→ `{{REVIEW_KDY}}`, `{{UDRZBA_KDY}}`, `{{DIGEST_CAS}}`, `{{DIGEST_TEMATA}}`

**G9. Od kdy se má denní vstup zpracovávat?** *(výchozí)*
Při prvním běhu by Claude vzal až 7 dní zpětně, včetně nahrávek a mailů,
o kterých jste nemluvili. Návrh: „Od zkušebního vstupu ve fázi 4.“
→ řádek `Start: RRRR-MM-DD hh:mm` v `00-System/VSTUP_STAV.md` (zapisuje
se ve fázi 4)

### H. Nástroje

**H1. E-mail a kalendář: které účty?** (pracovní, osobní; Google,
Microsoft, jiný)
Podle 03: **pracovní mail a kalendář na osobní účet Claude jen se
souhlasem firmy.** Bez pracovního kalendáře sekce Dnes v briefu vznikne
z toho, co řekne v denním vstupu („zítra mám…“), nebo se vynechá.
→ konektory (`03_nastaveni.md` část C)

**H2. Fakturace a účetnictví** (P, F): v čem fakturuješ a co z toho chceš
vědět?
Návrh: „Neuhrazené faktury a kdo je po splatnosti.“ Když pro nástroj
konektor v adresáři není, zapiš do `SETUP.md` → Otevřené a nic neslibuj.
Přístupové údaje nikdy do chatu.
→ `10-Firmy/`, `SETUP.md`

**H3. Další nástroje?** CRM, úkoly (Asana, Trello, Notion), chat (Slack,
Teams), sdílené disky. Jen zapsat; konektor jen když ho reálně použije.
→ konektory, `MI.md` Nástroje (`{{NASTROJE}}`)

**H4. Píšeš posty nebo obsah** (LinkedIn, newsletter, web)?
Návrh, když ano: „Týdenní review vybere 2 až 3 příběhy z týdne (bez jmen
lidí bez jejich souhlasu) do `40-Znalosti/Obsah_Suroviny.md`.“
→ Týdenní review (`{{OBSAH}}`: `ano` / `ne`)

### I. Dokumenty (P, F, OBCHOD; ostatním jen když zmíní)

**I1. Jaké dokumenty posíláš ven a jak je evidujete?** (nabídky,
smlouvy, reporty)
Návrh: „Verze v názvu (`_v2`) a datum, odeslané se nepřepisuje, v zakázce
tabulka Odeslané dokumenty. Odeslání nahlásím slovem ‚odesláno‘.“
→ `SKILL_MAP.md` workflow 6, šablona Zakazka

### J. Soukromí a firemní data

**J1. Co je citlivé a nesmí nikdy ven?**
Návrh: „Osobní věci a rodina, zdraví, peníze, hodnocení lidí, osobní
údaje klientů.“
→ `{{CITLIVE}}`: `CLAUDE.md`, `VAULT_MAP.md`, `CLAUDE_RULES.md`

**J2. Oddělení firem** (VÍC): co z jedné firmy nesmí do výstupů jiné?
Návrh: „Klienti, ceny a lidi jedné firmy nikdy do dokumentů jiné, bez
mého výslovného pokynu.“
→ `{{ODDELENI_FIREM}}`. Bez VÍC: „Mám jednu firmu, oddělení neřeším.“

**J3. Osobní část.** *(výchozí)* Deník v `50-Osobni/` bude vždy (je
citlivý). Chce tam i další osobní věci (zdraví, rodina, finance), nebo
jen deník? Návrh: „Zatím jen deník.“
→ `VAULT_MAP.md` (`{{OSOBNI}}`)

*(Firemní data, účty a zálohy už padly v otázkách 03 a 04.)*

### K. Kontrola úplnosti

Na konci: „Nedotkli jsme se něčeho, co by tvůj druhý mozek měl vědět?
Nějaká firma, člověk, opakovaná věc, kterou děláš každý týden?“

## Struktura souboru s rozhovorem

```
# Setup druhého mozku: rozhovor
Datum: RRRR-MM-DD · Cíl: podklady pro stavbu vaultu · Profil: …

## Souhrn (průběžně přepisovat)

## Odpovědi
### 01 Profil
- Zachyceno: …
- Doptáno: …

## Otevřené otázky
- [ ] … (kdo to ví)
```
