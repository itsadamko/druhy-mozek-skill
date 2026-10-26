# VSTUP_STAV: zpracované vstupy

*Založeno: {{DATUM}} • Zapisuje ranní zpracování a Claude při ruční práci
(check-in, přepis vložený do session). Podle tohohle souboru se pozná, co
už zpracované je, aby se nic nezapsalo dvakrát. Nejnovější nahoře. Řádky
neupravovat ručně, jen když se něco zpracovalo špatně: pak řádek smazat
a ranní zpracování položku vezme znovu.*

**Formát:** `ID` · datum vzniku · zdroj (`plaud` / `mail` / `prepis` /
`session`) · typ (`hlasovka` / `schuzka` / `checkin` / `preskoceno` /
`chyba`) · kam zapsáno (wikilinky)

ID = ID nahrávky, ID mailu, název souboru přepisu, nebo u check-inu
`checkin-RRRR-MM-DD-hhmm`.

Pod čarou je jako první řádek `Start:` (zapisuje se při setupu, fáze 4),
nové řádky přibývají hned pod ním.

---

