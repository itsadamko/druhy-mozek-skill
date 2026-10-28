# Nastavení: Obsidian, složka, zálohy, Claude projekt, konektory

Kroky dávej po jednom. Názvy tlačítek se mezi verzemi appek mění. Když
nesedí, nech uživatele popsat, co vidí, a veď ho podle toho. Nikdy
příkazy do Terminálu.

**ChatGPT Work:** části A1, A2 a A4 platí stejně. Místo A3, B, C a D
jede podle `06_chatgpt_work.md`.

## A. Obsidian, složka, zálohy

**A1. Obsidian.** obsidian.md → Download → nainstalovat. Zdarma, účet
není potřeba. Placený Obsidian Sync **není potřeba** (zálohy řeší A4).

**A2. Kde bude vault.** Složka nesmí ležet tam, kde ji systém umí
„odložit do cloudu“ (soubor pak na disku fyzicky není a Claude ho
nepřečte).
- **Mac:** Nastavení systému → (jméno / Apple ID) → iCloud → iCloud Drive
  → je zapnuté **Složky Plocha a Dokumenty**? Když ano, dát vault do
  domovské složky (`/Users/<jméno>/Vault`), ne do Dokumentů. Když ne,
  klidně do Dokumentů.
- **Windows:** je složka Dokumenty v OneDrivu (v Průzkumníku má ikonku
  mráčku nebo cestu s „OneDrive“)? Když ano, dát vault do
  `C:\Users\<jméno>\Vault`. Když ne, klidně do Dokumentů.

Pak: Obsidian → Create new vault → název `Vault` → umístění podle výsledku
→ Create.

**A3. Připojení složky v Coworku.** V Coworku (desktopová appka) vybrat
složku `Vault` jako pracovní složku session. Bez připojené složky nejde
nic zapsat. Do `SETUP.md` zapsat **cestu, jak ji vidí počítač**, nikdy
cestu, kterou Claude vidí v shellu (`/sessions/…`).

**A4. Zálohy přes Google Disk (doporučené, řeší se ve fázi 3).**
Až po otázkách 03 a 04 z rozhovoru: když firma AI nebo osobní úložiště
zakazuje (nebo to neví), nezálohovat firemní obsah na osobní disk. Na
firemním počítači může instalaci blokovat IT, pak jen zapsat do
`SETUP.md` → Otevřené.
1. Nainstalovat **Google Drive pro desktop** a přihlásit účet, na který
   se má zálohovat (otázka 04: typicky osobní).
2. Předvolby Disku → Můj počítač → Přidat složku → vybrat `Vault` →
   Synchronizovat s Diskem Google.
3. Ověřit: drive.google.com → Počítače → je tam Vault se soubory.
4. Pravidla: nikdy současně Obsidian Sync a Disk na stejné složce
   (vznikají duplikáty). Na dvou počítačích nepracovat naráz.

Jiná záloha (Time Machine, OneDrive mimo vault, externí disk) je taky
v pořádku. Hlavní je, aby vault nežil jen na jednom disku.

## B. Claude projekt „Druhý mozek“

1. V appce Claude → Projekty → Nový projekt → název **Druhý mozek**.
   Když setup už v projektu Druhý mozek běží, tenhle krok přeskoč.
2. Na týmovém nebo firemním účtu nech projekt **soukromý**.
3. Do instrukcí projektu vlož text níže (doplň `{{MENTOR_HLIDA}}` stejně
   jako v `CLAUDE.md`). Dej ho v bloku, ať ho jen zkopíruje:

```
Na začátku každé session si nejdřív přečti CLAUDE.md v kořeni mého vaultu (připojená složka Vault) a řiď se jím. Definuje tvou roli (druhý mozek, mentor, parťák pro plánování) a odkazuje na pravidla v 00-System/ (VAULT_MAP, SKILL_MAP, MI s rozhodovacím filtrem, CLAUDE_RULES, ULOHY, DASHBOARD, BRIEF).
Nejdůležitější pravidlo: hlídej {{MENTOR_HLIDA}}. Každou novou zakázku, projekt nebo závazek prověř filtrem z 00-System/MI.md. Buď ke mně upřímný a přímý, ne servilní. Rozhoduju já, ty radíš.
Když ti něco řeknu nebo nadiktuju, roztřiď to do vaultu sám (lidi, sliby, zakázky, projekty, deník) a jednou větou řekni, kam to šlo.
Když session nemá připojenou složku Vault, řekni mi to hned na začátku.
```

4. **Od teď:** každá práce se vaultem = Cowork session **v projektu
   Druhý mozek + připojená složka Vault.** Bez projektu Claude instrukce
   nevidí, bez složky nemá kam sáhnout.
5. **Paměť:** v Coworku funguje jen uvnitř projektu. Když v nastavení
   projektu nebo appky vidí paměť vypnutou a chce ji, ať ji zapne. Vault
   je stejně hlavní paměť, tahle je jen pomocná.

## C. Konektory

Připojit **před** založením naplánovaných úloh. Konektory: v appce
Customize (nebo Nastavení) → Konektory, nebo v session přes „+“. Jen to,
co reálně použije.

**Pracovní účty (mail, kalendář, disk) na osobní účet Claude jen se
souhlasem firmy** (otázka 03). Bez pracovního kalendáře se sekce Dnes
v briefu skládá z toho, co řekne v denním vstupu, nebo se vynechá.

| Konektor | K čemu | Pozn. |
|---|---|---|
| **Plaud** | hlasovky a schůzky čte ranní zpracování samo | když G1 = Plaud. Oficiální konektor v adresáři, přihlásit jeho Plaud účtem |
| **Gmail** (nebo Outlook) | mail sobě s předmětem „Hlasovka“, dohledat mail ke schůzce | když G1 = mail sobě, jinak volitelný. Outlook / Microsoft 365 jen když ho adresář na jeho tarifu nabízí |
| **Google Kalendář** (nebo Outlook) | brief ukáže dnešní schůzky s kontextem, deník vidí schůzky dne | **silně doporučený** |
| Google Drive | podklady, sdílené složky | volitelný |
| další z adresáře | podle H3 (CRM, úkoly, chat) | jen když se z nich má číst |

**Plaud v appce (jinak hlasovky nepojedou):** zapnout **automatický
přepis** nahrávek a jazyk **čeština**. Ověřit, kolik minut přepisu má
jeho tarif za měsíc: denní vstup a schůzky je musí pokrýt.

**Mail sobě:** domluvit **přesný předmět** „Hlasovka“ (bez dalších slov
na začátku) a **přesnou adresu** (`{{MAIL_ADRESA}}`). Ranní zpracování
čte jen maily z téhle adresy na tuhle adresu s tímhle předmětem, žádné
jiné (u Gmailu dotaz `from:<adresa> to:<adresa> subject:Hlasovka`).

**Ověření po připojení** (jedno čtení na konektor, výsledek zapsat do
`SETUP.md`):
- Kalendář: vypsat dnešní události.
- Mail sobě: ať si **z telefonu, přesně tou cestou, kterou bude
  používat** (diktování, odeslání z výchozího účtu), pošle zkušební
  Hlasovku. Najdi ji přes konektor uvedeným dotazem. Když ji nenajdeš,
  telefon posílá z jiného účtu: oprav adresu, nebo přepněte na
  check-in.
- Plaud: `list_files` vrátí jeho nahrávky, `get_transcript` u jedné
  z nich vrátí text přepisu (ne jen shrnutí). Když přepis nejde, záloha:
  v Plaud appce u nahrávky Sdílet / Export přepisu jako text do
  `05-Inbox/Prepisy/`. Zapsat do `SETUP.md` → Otevřené.

**Oprávnění:** úlohy běží bez dohledu, takže pojistka nemá být jen
v textu. U konektorů e-mailu a kalendáře (Customize → Konektory →
u konektoru oprávnění nástrojů) nastav nástroje, které **odesílají,
mažou nebo vytvářejí** (odeslat mail, smazat, vytvořit událost), na
**Blocked / Zablokováno**. Koncepty mailů může nechat na „Needs
approval“, když je chce v session používat. Když appka takové nastavení
nenabízí, jen to zapiš do `SETUP.md` → Otevřené.

**Bez konektoru (zapsat, nic neslibovat):** nástroje, pro které
konektor v adresáři není (fakturace, firemní systémy), jen zapsat do
`MI.md` Nástroje a do `SETUP.md` → Otevřené. Přístupové údaje nikdy do
chatu ani do vaultu.

**Na firemním účtu Claude** může konektory povolovat správce organizace.
Když konektor v nabídce chybí, ať požádá správce.

## D. Provoz

- **Vault leží na počítači**, takže cokoli, co do něj zapisuje (session
  i naplánovaná úloha), potřebuje **zapnutý počítač a spuštěnou appku
  Claude**. Ranní čas volit, kdy je počítač reálně otevřený.
- Když appka nabízí volbu „nechat počítač vzhůru“ (Keep awake), pro
  automatické úlohy ji zapnout. Notebook se zavřeným víkem neudrží vzhůru
  nic.
- **Limity tarifu:** Cowork spotřebuje víc než běžný chat. Na tarifu Pro
  nezakládat moc automatických úloh; ranní zpracování má přednost, digest
  a údržba jsou bonus. Když narazí na limity, úlohy přepnout na menší
  model, nebo je pouštět jen na slovo.
- Plaud přepisuje až po synchronizaci z telefonu nebo zařízení. Když
  ranní zpracování nahrávku nevidí, bývá to tím, že se nesynchronizovala.
