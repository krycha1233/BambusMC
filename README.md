# BambusMC – Strona serwera Minecraft

Nowoczesna strona główna serwera **BambusMC** w stylu RareMC – jasna zieleń, czyste karty, mobilny UI.

**Adres serwera:** `bambusmc.gmht.pl`  
**Link do strony:** [krycha1233.github.io/BambusMC](https://krycha1233.github.io/BambusMC/)

---

## Pliki

| Plik | Opis |
|------|------|
| `index.html` | Główna strona (musi mieć tę nazwę na GitHub Pages) |
| `README.md` | Ten plik |

---

## Co się zmieniło (nowy design)

- **Jasne tło** w stylu RareMC (`#d4edc4`)
- Licznik **graczy online** z animowaną kropką
- Duży przycisk **Skopiuj IP**
- Karta **Doładowanie do /portfel** z suwakiem + nickiem
- Widok płatności jak w profesjonalnym sklepie:
  - BLIK (domyślny)
  - PaysafeCard
  - Kod rabatowy
  - Checkboxy zgód
  - Podsumowanie kwoty z VAT
- Pełny flow 2-ekranowy (home → płatność)

---

## Jak działa sklep

### Krok 1 – Home
- Suwak kwoty (1–1000 vPLN)
- Pole nicka
- Przycisk z papierowym samolotem → przechodzi do płatności

### Krok 2 – Płatność
- Nick + Discord
- Suwak kwoty
- Wybór metody: **BLIK** / **PaysafeCard**
- Kod rabatowy
- Zgody (wymagane)
- Podsumowanie „Do zapłaty”

#### 📱 BLIK
- Wysyła embed na **Discord webhook**
- Admin dostaje `@here` + szczegóły

#### 💳 PaysafeCard
- Formularz z kodem 16-cyfrowym
- Wysyła na mail `bambusmc67@gmail.com` przez FormSubmit

---

## Kody rabatowe

| Kod | Zniżka |
|-----|--------|
| `bambuswakacje` | **-10%** |
| `easyspust67` | **-30%** |

Kody są w `discountCodes` w JavaScript – możesz je swobodnie zmieniać.

---

## Discord Webhook (BLIK)

W `index.html`:

```js
const DISCORD_WEBHOOK = "https://discord.com/api/webhooks/...";
```

Webhook jest już ustawiony.

---

## Jak wrzucić na GitHub Pages

1. Skopiuj `index.html` do repozytorium **BambusMC**
2. Settings → Pages → Source: branch `main`
3. Odśwież po 1–2 minutach:  
   `https://krycha1233.github.io/BambusMC/`

---

## Uwagi

- FormSubmit (PSC) – pierwsze wysłanie może wymagać potwierdzenia maila.
- BLIK wymaga poprawnego webhooka Discord.
- Zgody są wymagane przy obu metodach.
- Adres serwera: **bambusmc.gmht.pl**
