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

## Jak działa sklep

### Krok 1 – Home
- Suwak kwoty (1–1000 vPLN)
- Pole nicka
- Przycisk **„Przejdź do płatności”**

### Krok 2 – Wybór metody
- Nick, Discord, **e-mail gracza** (wymagany)
- Suwak kwoty
- Wybór: **BLIK** lub **PaysafeCard**
- Kod rabatowy
- Checkboxy zgód
- Podsumowanie kwoty

### Krok 3 – PaysafeCard (osobna strona)
Po wyborze PSC gracz trafia na stronę w stylu oficjalnej Paysafecard:
- 16-cyfrowy kod
- E-mail gracza
- Akceptacja warunków
- Przycisk **Płatność**

Powiadomienie leci na mail: **bambusmc67@gmail.com**

### BLIK
- Wysyła embed na **Discord webhook**
- Admin dostaje `@here` + szczegóły (nick, e-mail, kwota, rabat)

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

## Mail PSC (FormSubmit)

Formularz Paysafecard wysyła na:

```
bambusmc67@gmail.com
```

W mailu dostajesz:
- Nick gracza
- Discord
- E-mail gracza
- Kod PSC (16 cyfr)
- Kwotę oryginalną i po rabacie
- Kod rabatowy (jeśli był)

**Uwaga:** FormSubmit tylko wysyła maila z kodem. Kod PSC musisz **ręcznie zrealizować** na [paysafecard.com](https://www.paysafecard.com), a potem doładować graczowi vPLN na serwerze.

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
- E-mail gracza i zgody są wymagane.
- Adres serwera: **bambusmc.gmht.pl**
