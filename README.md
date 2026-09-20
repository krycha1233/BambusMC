# BambusMC – Strona serwera Minecraft

Strona główna serwera **BambusMC** (Aternos) z formularzem doładowania /portfel przez Paysafecard.

## Pliki

- `bambus-index.html` – gotowa strona (wystarczy wrzucić na hosting / GitHub Pages / Netlify)
- `bambus-readme.md` – ten plik z instrukcją

## Jak działa sklep (2 kroki)

### Krok 1 – Wybór kwoty
Na stronie sklepu widać tylko:
- Suwak z wyborem **vPLN**
- Przycisk **„Przejdź do płatności”**

### Krok 2 – Formularz płatności
Po kliknięciu „Przejdź do płatności” pojawia się osobny widok z:
- Wybraną kwotą
- Nickiem gracza
- Nickiem Discord
- Kodem Paysafecard (PSC)
- Opcjonalnym kodem rabatowym
- Przyciskiem **„Wyślij doładowanie PSC”**

Można wrócić przyciskiem **„← Wróć do wyboru kwoty”**.

## Kody rabatowe

| Kod              | Zniżka |
|------------------|--------|
| `bambuswakacje`  | **-10%** |
| `easyspust67`    | **-30%** |

Kody działają na stronie płatności. Po wpisaniu poprawnego kodu kwota automatycznie się zmniejsza.

## Co dostajesz w mailu (FormSubmit)

Po wysłaniu formularza na `bambusmc67@gmail.com` dostajesz:
- Nick gracza
- Nick Discord
- Kod PSC
- Oryginalną kwotę (Kwota_vPLN)
- Kod rabatowy (jeśli podany)
- Procent rabatu
- **Kwotę po rabacie** (Kwota_po_rabacie)

## Jak wrzucić na stronę

1. Weź plik `bambus-index.html`
2. Wrzuć go na swój hosting (lub GitHub Pages / Netlify / Cloudflare Pages)
3. Gotowe – strona działa od razu

## Uwagi

- Formularz korzysta z [FormSubmit](https://formsubmit.co) – pierwsze wysłanie może wymagać potwierdzenia maila.
- Kody rabatowe są w kodzie JavaScript (sekcja `discountCodes`). Możesz je dowolnie zmieniać / dodawać.
- Discord i nick są wymagane, kod rabatowy jest opcjonalny.
