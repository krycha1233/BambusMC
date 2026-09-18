# 🎋 BambusMC

Strona internetowa serwera Minecraft **BambusMC** — prosta, jednoplikowa strona (HTML + CSS + JS), gotowa do hostowania przez **GitHub Pages**.

## Podgląd

Strona zawiera:
- pasek nawigacji z linkiem do Discorda,
- sekcję hero z adresem IP serwera i przyciskiem "Skopiuj IP",
- sekcję sklepu serwerowego z linkiem do zewnętrznego, bezpiecznego systemu płatności (Tebex),
- responsywny układ (mobile-friendly).

## Struktura repozytorium

```
.
├── index.html   # cała strona (HTML, CSS, JS w jednym pliku)
└── README.md    # ten plik
```

## Jak uruchomić lokalnie

Wystarczy otworzyć plik `index.html` w przeglądarce — strona nie wymaga żadnego backendu ani instalacji zależności.

## Jak wystawić stronę na GitHub Pages

1. Utwórz nowe repozytorium na GitHubie (np. `bambusmc`) i wrzuć do niego pliki `index.html` oraz `README.md`.
2. Wejdź w repozytorium → **Settings** → **Pages**.
3. W sekcji **Build and deployment** → **Source** wybierz **Deploy from a branch**.
4. Jako **Branch** wybierz `main` (lub `master`) i folder `/ (root)`, następnie kliknij **Save**.
5. Po chwili strona będzie dostępna pod adresem:
   ```
   https://<twoja-nazwa-użytkownika>.github.io/<nazwa-repozytorium>/
   ```

## Konfiguracja przed publikacją

Przed wdrożeniem zmień w `index.html`:
- link do Discorda (`href="https://discord.gg/"`) na zaproszenie do swojego serwera,
- adres IP serwera (`bambusmc.aternos.me`) na aktualny adres,
- link do sklepu (`https://TWOJ-SKLEP.tebex.io`) na adres swojego sklepu Tebex (lub innego legalnego systemu płatności).

## ⚠️ Ważna uwaga dotycząca płatności

Sekcja sklepu **celowo nie zbiera** kodów kart przedpłaconych (np. Paysafecard) przez formularz wysyłany mailem — taki mechanizm jest typową metodą oszustw i nie stanowi bezpiecznej weryfikacji płatności. Zamiast tego strona kieruje graczy do zewnętrznego, sprawdzonego systemu płatności (np. [Tebex](https://www.tebex.io/)), który obsługuje karty, BLIK i inne metody bez ręcznego przekazywania kodów kart.

## Licencja

Projekt do własnego, dowolnego wykorzystania na potrzeby serwera BambusMC.
