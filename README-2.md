# BambusMC – Strona serwera Minecraft

Strona główna serwera **BambusMC** (Aternos) z formularzem doładowania `/portfel` przez Paysafecard.

**Link do strony:** [krycha1233.github.io/BambusMC](https://krycha1233.github.io/BambusMC/)

---

## Pliki

| Plik | Opis |
|------|------|
| `index.html` | Główna strona (musi mieć tę nazwę, żeby GitHub Pages działał) |
| `README.md` | Ten plik |

> **Ważne:** Na GitHub Pages plik musi nazywać się dokładnie `index.html`.  
> Jeśli masz `bambus-index.html` → zmień nazwę na `index.html`.

---

## Jak działa sklep (2 kroki)

### Krok 1 – Wybór kwoty
Na stronie sklepu widać tylko:
- Suwak z wyborem **vPLN**
- Przycisk **„Przejdź do płatności”**

### Krok 2 – Formularz płatności
Po kliknięciu pojawia się **osobny pełny ekran** z:
- Wybraną kwotą
- Nickiem gracza
- Nickiem Discord
- Kodem Paysafecard (PSC)
- Opcjonalnym kodem rabatowym
- Przyciskiem **„Wyślij doładowanie PSC”**

Przycisk **„← Wróć do wyboru kwoty”** wraca do kroku 1.

---

## Kody rabatowe

| Kod | Zniżka |
|-----|--------|
| `bambuswakacje` | **-10%** |
| `easyspust67` | **-30%** |

Kody działają na stronie płatności. Po wpisaniu poprawnego kodu kwota automatycznie się zmniejsza.

Kody są ukryte w kodzie JavaScript (sekcja `discountCodes`) – możesz je dowolnie zmieniać / dodawać.

---

## Co dostajesz w mailu (FormSubmit)

Po wysłaniu formularza na **bambusmc67@gmail.com** dostajesz:

- Nick gracza  
- Nick Discord  
- Kod PSC  
- Oryginalną kwotę (`Kwota_vPLN`)  
- Kod rabatowy (jeśli podany)  
- Procent rabatu  
- **Kwotę po rabacie** (`Kwota_po_rabacie`)

---

## Jak wrzucić / zaktualizować stronę

1. Weź plik `index.html`
2. Wrzuć go do repozytorium **BambusMC** (zamień stary plik)
3. Upewnij się, że w Settings → Pages jest włączone GitHub Pages (branch: `main` / `główny`)
4. Po 1–2 minutach odśwież:  
   `https://krycha1233.github.io/BambusMC/`

---

## Uwagi

- Formularz korzysta z [FormSubmit](https://formsubmit.co) – **pierwsze** wysłanie może wymagać potwierdzenia maila (sprawdź skrzynkę `bambusmc67@gmail.com`).
- Discord i nick są **wymagane**, kod rabatowy jest opcjonalny.
- Po przejściu do płatności znika cała reszta strony (top bar, hero, footer) – zostaje tylko formularz.
