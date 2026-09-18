# BambusMC – Strona serwera Minecraft

Strona główna serwera **BambusMC** (Aternos) z formularzem doładowania /portfel przez Paysafecard.

## Pliki

- `index.html` – gotowa strona (wystarczy wrzucić na hosting / GitHub Pages / Netlify)

## Co zostało dodane

### 1. Pole Discord
Pod nickiem gracza jest wymagane pole na **nick Discord**.

### 2. Kody rabatowe
Pod kodem PSC jest opcjonalne pole **Kod rabatowy**.

| Kod              | Zniżka |
|------------------|--------|
| `bambuswakacje`  | **-10%** |
| `easyspust67`    | **-30%** |

**Jak działa rabat:**
- Gracz wybiera np. **10 vPLN**
- Wpisuje kod `bambuswakacje`
- System odejmuje 10% → **płaci 9 vPLN**
- Główna kwota na stronie od razu się zmienia
- Widać komunikat: *Było: 10 vPLN → Płacisz: 9 vPLN*

Kody są **niewidoczne** na stronie – znają je tylko osoby, którym je podasz.

### 3. Co dostajesz w mailu (FormSubmit)
Po wysłaniu formularza na `bambusmc67@gmail.com` dostajesz:
- Nick gracza
- Nick Discord
- Kod PSC
- Oryginalną kwotę (Kwota_vPLN)
- Kod rabatowy (jeśli podany)
- Procent rabatu
- **Kwotę po rabacie** (Kwota_po_rabacie)

## Jak wrzucić na stronę

1. Weź plik `index.html`
2. Wrzuć go na swój hosting (lub GitHub Pages / Netlify / Cloudflare Pages)
3. Gotowe – strona działa od razu

## Uwagi

- Formularz korzysta z [FormSubmit](https://formsubmit.co) – pierwsze wysłanie może wymagać potwierdzenia maila.
- Kody rabatowe są w kodzie JavaScript (sekcja `discountCodes`). Możesz je dowolnie zmieniać / dodawać.
- Discord i nick są wymagane, kod rabatowy jest opcjonalny.
