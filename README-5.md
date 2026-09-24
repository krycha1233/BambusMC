# BambusMC – Strona serwera Minecraft

Strona główna serwera **BambusMC** (Aternos) z formularzem doładowania `/portfel` przez **Paysafecard** i **BLIK**.

**Link do strony:** [krycha1233.github.io/BambusMC](https://krycha1233.github.io/BambusMC/)

---

## Pliki

| Plik | Opis |
|------|------|
| `index.html` | Główna strona (musi mieć tę nazwę, żeby GitHub Pages działał) |
| `README.md` | Ten plik |

> **Ważne:** Na GitHub Pages plik musi nazywać się dokładnie `index.html`.

---

## Jak działa sklep (2 kroki)

### Krok 1 – Wybór kwoty
- Suwak z wyborem **vPLN**
- Pole do **wpisania** dokładnej kwoty (1–1000)
- Przycisk **„Przejdź do płatności”**

### Krok 2 – Wybór metody + formularz
Po kliknięciu pojawia się wybór:

#### 💳 Paysafecard (PSC)
- Nick gracza
- Nick Discord
- Kod Paysafecard (16 cyfr)
- Opcjonalny kod rabatowy
- Wysyła na **mail** (`bambusmc67@gmail.com`) przez FormSubmit

#### 📱 BLIK
- Nick gracza
- Nick Discord
- Opcjonalny kod rabatowy
- **Bez kodu PSC**
- Po kliknięciu „Wyślij” leci **powiadomienie na Discord** (webhook)

Przycisk **„← Wróć do wyboru kwoty”** wraca do kroku 1.

---

## Kody rabatowe

| Kod | Zniżka |
|-----|--------|
| `bambuswakacje` | **-10%** |
| `easyspust67` | **-30%** |

Kody działają w obu metodach. Po wpisaniu poprawnego kodu kwota automatycznie się zmniejsza.

Kody są w kodzie JavaScript (sekcja `discountCodes`) – możesz je zmieniać / dodawać.

---

## Discord Webhook (dla BLIK)

W pliku `index.html` znajdź linię:

```js
const DISCORD_WEBHOOK = "https://discord.com/api/webhooks/TWOJ_ID/TWOJ_TOKEN";
```

Zamień na swój prawdziwy webhook (Server Settings → Integrations → Webhooks → New Webhook → Copy Webhook URL).

Bez tego BLIK nie wyśle powiadomienia.

---

## Co dostajesz

### Przy PSC (mail)
- Nick gracza  
- Nick Discord  
- Kod PSC  
- Oryginalną kwotę  
- Kod rabatowy (jeśli podany)  
- Procent rabatu  
- Kwotę po rabacie  
- Metodę: Paysafecard

### Przy BLIK (Discord)
Embed z:
- Nick gracza
- Discord
- Kwota oryginalna + po rabacie
- Rabat / kod rabatowy
- Metoda: BLIK

---

## Jak wrzucić / zaktualizować stronę

1. Weź plik `index.html`
2. Wrzuć go do repozytorium **BambusMC** (zamień stary plik)
3. Upewnij się, że w Settings → Pages jest włączone GitHub Pages (branch: `main`)
4. Po 1–2 minutach odśwież:  
   `https://krycha1233.github.io/BambusMC/`

---

## Uwagi

- Formularz PSC korzysta z [FormSubmit](https://formsubmit.co) – pierwsze wysłanie może wymagać potwierdzenia maila.
- BLIK wymaga ustawionego webhooka Discord.
- Discord i nick są wymagane w obu metodach.
- Po przejściu do płatności znika cała reszta strony – zostaje tylko formularz.
