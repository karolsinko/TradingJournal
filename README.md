# TradingJournal — KryptoDesk

Jednosúborová (`index.html`) krypto trading dashboard a trade journal. Beží čisto v prehliadači — žiadny build, žiadny server, dáta z Binance a alternative.me API.

## Záložky
- **Prehľad** — ceny, heatmapa trhu, Fear & Greed, denný bias, čisté obchodné imanie
- **Analýza** — technická analýza BTC/ETH, trhový režim, úrovne podpory/odporu
- **Signály** — long/short setupy so vstupom/stopom/cieľmi
- **DCA** — skóre "zľavy od maxima" pre nákupné príležitosti
- **Sledované** — watchlist s cenovými upozorneniami (toast + browser notifikácie)
- **Portfólio (HODL)** — spot holdingy, alokácia, cieľ portfólia, upozornenie na koncentráciu rizika
- **Trade log (Futures)** — trade journal s R-multiple, expectancy, kalendárom P&L, risk kalkulačkou
- **Dáta a záloha** — cloud synchronizácia + história verzií + manuálny JSON/CSV export-import

## Ukladanie dát
Dáta sa primárne ukladajú do `localStorage` prehliadača — to je viazané na konkrétny prehliadač/zariadenie. Aby trade logy neprišli o dáta pri zmene zariadenia, vyčistení dát prehliadača a pod., appka podporuje:

1. **Cloud sync cez Firebase** (záložka Dáta a záloha) — appka zálohuje holdingy, pozície a watchlist do tvojej vlastnej bezplatnej Firebase (Firestore) databázy. Žiadny token — len skopírované API Key + Project ID z Firebase konzoly a vygenerované ID dokumentu (funguje ako heslo). Synchronizuje sa v reálnom čase naprieč zariadeniami.
2. **História lokálnych verzií** — posledných 15 zmien sa ukladá lokálne, s možnosťou obnovy jedným klikom.
3. **Manuálny JSON export/import** — kompletná záloha na stiahnutie/nahratie.
4. **CSV export/import** pozícií.

## Poznámka
Automatické technické signály a analýzy sú heuristiky počítané z verejných trhových dát — nie sú to investičné odporúčania.
