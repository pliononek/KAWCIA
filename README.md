# ☕ KAWCIA – śledzenie makro przy po mocy AI za DARMO

**KAWCIA** to nowoczesna, lekka i w pełni lokalna aplikacja webowa (PWA) stworzona z myślą o urządzeniach mobilnych. Pozwala w wygodny sposób śledzić spożyte kalorie, makroskładniki oraz historię posiłków.

Aplikacja stawia na **prywatność** – wszystkie Twoje dane są zapisywane wyłącznie na Twoim urządzeniu, żadne dane nie trafiają na serwer.

**Aktualna wersja: 2.1.0**

---

## ✨ Funkcje

- **📊 Licznik kalorii** — czytelny pierścień postępu z budżetem kalorycznym, statusem dnia („W normie” / przekroczony cel) i liczbą posiłków
- **🥩 Makroskładniki** — białko, węglowodany i tłuszcze z paskami postępu względem Twoich celów
- **🤖 Analiza AI** — dodaj posiłek przez opis tekstowy, zdjęcie (aparat lub galeria) albo skan kodu kreskowego EAN
- **⭐ Ulubione posiłki** — zapisuj ulubione dania i dodawaj je jednym dotknięciem z okna dodawania posiłku
- **📅 Przegląd tygodnia** — wykres ostatnich 7 dni na ekranie głównym
- **🗂️ Historia** — archiwum posiłków według dni z podsumowaniem kalorii i makro
- **📤 Eksport CSV** — pobierz wszystkie wpisy do arkusza
- **📚 Open Food Facts** — wyszukiwarka produktów i baza wartości odżywczych dla AI (przełącznik w Ustawieniach)
- **🎨 Motywy** — jasny i ciemny (z automatycznym dopasowaniem do ustawień systemu)
- **🔄 Auto-aktualizacja** — aplikacja sprawdza nowe wersje na GitHubie i podmienia się przy następnym uruchomieniu
- **📱 PWA** — działa jak natywna aplikacja po dodaniu do ekranu głównego
- **🔒 Privacy-First** — zero konta, zero serwera, dane tylko w `localStorage`
- **📳 Wibracje** — delikatny feedback haptyczny przy akcjach (na urządzeniach, które to wspierają)

---

## 🤖 Modele AI (Google Gemini)

Aplikacja używa **Google Gemini** jako dostawcy AI. Klucz API jest darmowy.

| Model | Rola | RPM | RPD | Zdjęcia |
|---|---|---|---|---|
| `gemini-3.1-flash-lite` ⭐ | domyślny | 15 | 500 | ✅ |
| `gemini-3.5-flash-lite` | fallback | 15 | 500 | ✅ |
| `gemini-2.5-flash` | do wyboru | 5 | 20 | ✅ |
| `gemini-2.5-flash-lite` | do wyboru | 10 | 20 | ✅ |

> ❗Nie dodawałem GPT ani Anthropic — było z nimi za dużo błędów, a Gemini API jest darmowe, więc dla przeciętnego użytkownika to w zupełności wystarczy.

> 💡 Aplikacja domyślnie startuje od **gemini-3.1-flash-lite** — najszybszy model i najwięcej darmowych zapytań dziennie (500/dzień).

**Automatyczny fallback:** jeśli wybrany model zwróci błąd (limit, przeciążenie, wycofanie modelu), aplikacja po kolei próbuje kolejnych modeli z listy — najpierw `gemini-3.5-flash-lite`, potem pozostałych. Nie musisz nic robić ręcznie.

> ⚠️ Limity RPM/RPD pochodzą z darmowego planu Google i mogą się zmieniać. Aktualne wartości sprawdzisz w dokumentacji Gemini API.

---

## 🔑 Krok po kroku: jak zdobyć darmowy klucz API Gemini

> Bez klucza API aplikacja nie będzie mogła analizować posiłków przez AI (ręczne dodawanie i skan EAN działają bez klucza). Zajmuje to **2 minuty** i jest całkowicie darmowe.

**Krok 1** — Wejdź na stronę 👉 [aistudio.google.com](https://aistudio.google.com)

**Krok 2** — Kliknij **„Sign in”** i zaloguj się swoim kontem Google (tym samym co Gmail)

**Krok 3** — Po zalogowaniu kliknij niebieski przycisk **„Get API key”** w lewym górnym rogu

**Krok 4** — Kliknij **„Create API key”** → wybierz **„Create API key in new project”**

**Krok 5** — Pojawi się długi ciąg znaków (np. `AIzaSy...`). Kliknij ikonkę kopiowania obok niego

**Krok 6** — Otwórz KAWCIA → wejdź w **Ustawienia** → wklej klucz w pole **„Klucz API Gemini”** → wybierz model → **„Zapisz ustawienia”**

> ⚠️ Klucz to jak hasło — nie pokazuj go nikomu i nie wklejaj na publicznych stronach.

---

## 🚀 Instalacja — krok po kroku

### 📱 iPhone (Safari)

**Krok 1** — Otwórz Safari i wejdź na:
```
https://pliononek.github.io/KAWCIA/
```

**Krok 2** — Na dole ekranu kliknij ikonkę **Udostępnij** (kwadrat ze strzałką w górę ↑)

**Krok 3** — Przewiń listę w dół i kliknij **„Dodaj do ekranu początkowego”**

**Krok 4** — Kliknij **„Dodaj”** w prawym górnym rogu

**Krok 5** — Na pulpicie pojawi się ikona KAWCIA ☕ — otwieraj ją jak normalną aplikację!

> ⚠️ Używaj **Safari** — tylko Safari na iOS obsługuje dodawanie PWA do ekranu głównego. Chrome i Firefox na iPhonie tego nie umożliwiają.

---

### 🤖 Android (Chrome)

**Krok 1** — Otwórz Chrome i wejdź na:
```
https://pliononek.github.io/KAWCIA/
```

**Krok 2** — Kliknij trzy kropki ⋮ w prawym górnym rogu

**Krok 3** — Wybierz **„Dodaj do ekranu głównego”** lub **„Zainstaluj aplikację”**

**Krok 4** — Kliknij **„Dodaj”** — gotowe!

---

### 💻 Komputer (przeglądarka)

Wejdź na [https://pliononek.github.io/KAWCIA/](https://pliononek.github.io/KAWCIA/) — działa od razu, bez instalacji.

---

## 🖥️ Własny serwer lokalny

### 🐧 Linux (Ubuntu / Debian / Arch / CachyOS)

```bash
# Zainstaluj nginx
sudo apt install nginx        # Ubuntu/Debian
sudo pacman -S nginx          # Arch/CachyOS

# Skopiuj plik aplikacji
sudo cp index.html /usr/share/nginx/html/index.html

# Uruchom nginx
sudo systemctl enable --now nginx

# Aplikacja dostępna pod:
# http://localhost          — lokalnie
# http://TWOJE_IP           — w sieci domowej (sprawdź IP przez: ip a)
```

> Na Archu/CachyOS katalogiem domyślnym nginx jest zwykle `/usr/share/nginx/html`, a usługa nazywa się `nginx`.

---

### 🪟 Windows

**Opcja 1 — Python (najprościej):**
```cmd
cd C:\ścieżka\do\folderu\z\index.html
python -m http.server 8080
```
Wejdź na `http://localhost:8080`

**Opcja 2 — nginx:**
1. Pobierz nginx ze strony [nginx.org/en/download.html](https://nginx.org/en/download.html)
2. Wypakuj ZIP, skopiuj `index.html` do folderu `html/`
3. Uruchom `nginx.exe` → wejdź na `http://localhost`

---

### 🍎 macOS

```bash
# Python (nie wymaga instalacji)
cd /ścieżka/do/folderu
python3 -m http.server 8080
# Wejdź na http://localhost:8080

# lub nginx przez Homebrew
brew install nginx
cp index.html /opt/homebrew/var/www/index.html   # Apple Silicon
# cp index.html /usr/local/var/www/index.html    # Intel
brew services start nginx
```

---

### 🌐 Udostępnienie przez internet (opcjonalne)

1. Sprawdź swoje publiczne IP: `curl ifconfig.me`
2. W routerze ustaw **port forwarding**: port `80` → Twój lokalny IP
3. Darmowa domena: [duckdns.org](https://duckdns.org)
4. HTTPS: [certbot.eff.org](https://certbot.eff.org)

> ⚠️ Aparat (skanowanie kodów i zdjęcia posiłków) działa tylko przez HTTPS lub `localhost`. Przez zwykłe HTTP Safari zablokuje dostęp do kamery.

---

## 🔄 Aktualizacje

KAWCIA potrafi aktualizować się sama — bez sklepów z aplikacjami.

- Po uruchomieniu (po ~3 s) aplikacja sprawdza najnowsze wydanie w GitHub Releases repozytorium `pliononek/KAWCIA`
- nowy `index.html` jest pobierany i zapisywany w `localStorage` (`cal_updatedHtml`), a podmieniany przy **następnym** otwarciu aplikacji
- status i wersję widzisz w **Ustawienia → Aktualizacje** („Obecna wersja”, „Najnowsza wersja”), tam też jest przycisk **„Sprawdź”** i **„Zainstaluj”**
- auto-sprawdzanie można wyłączyć przełącznikiem **„Auto-aktualizacja przy starcie”**

**Ważne dla autora:** numer wersji w release (np. tag `v2.1.0` albo nazwa `2.1.0`) musi być **wyższy** niż `APP_VERSION` w kodzie, inaczej aktualizacja nie zostanie zaproponowana. Aplikacja czyści stary cache HTML, gdy wersja w kodzie jest nowsza lub równa wersji cache — dzięki temu świeżo wgrany plik nigdy nie zostanie nadpisany starą kopią z `localStorage`.

---

## 🛠️ Technologie

Czysty HTML + CSS + JavaScript w jednym pliku — zero frameworków, zero buildu, zero zależności do instalacji.

- **HTML5 / CSS3 / Vanilla JS (ES6+)**
- **Web Storage API** (`localStorage`) — dane użytkownika, ustawienia, cache aktualizacji
- **Google Gemini API** — analiza posiłków (tekst i zdjęcia)
- **ZXing** (ładowany z CDN) — skanowanie kodów kreskowych EAN
- **Open Food Facts API** — wyszukiwarka produktów i wartości odżywcze
- **GitHub Releases API** — auto-aktualizacja
- **Web Vibration API** — feedback haptyczny
- **Google Fonts** — DM Sans i Manrope

---

## 🔒 Prywatność

- brak konta, brak backendu, brak analityki
- posiłki, cele, ulubione i klucz API trzymane wyłącznie w `localStorage` Twojej przeglądarki
- dane sieciowe wychodzą tylko wtedy, gdy sam ich zażądasz: zapytanie do Gemini (z Twoim kluczem), wyszukiwanie w Open Food Facts lub sprawdzanie aktualizacji na GitHubie
- „Wyczyść wszystkie dane” w Ustawieniach usuwa wszystko bezpowrotnie z urządzenia

---

## 👩‍💻 Dla deweloperów

Lista modeli występuje w trzech miejscach w `index.html` i trzeba je zmieniać razem:

1. `<select id="geminiModel">` — opcje widoczne w Ustawieniach
2. stałe `DEFAULT_GEMINI_MODEL`, `FALLBACK_GEMINI_MODEL` i tablica `GEMINI_MODELS`
3. migracja w `init()` — stare/nieznane modele są podmieniane na `DEFAULT_GEMINI_MODEL`

Każda zmiana logiki = podbicie `APP_VERSION` (inaczej mechanizm auto-aktualizacji pominie nową wersję).

---

## 📝 Licencja

**Kod źródłowy — MIT**
Cały kod (`index.html`, `README.md` itd.) jest dostępny na licencji MIT. Możesz go dowolnie modyfikować, forkować i używać.

**Ikona aplikacji — All Rights Reserved ⚠️**
Zdjęcie użyte jako ikona aplikacji jest chronione prawem autorskim i nie podlega licencji MIT. Zabronione jest kopiowanie, redystrybucja, modyfikacja oraz użycie komercyjne bez pisemnej zgody autora.

© 2026 Patryk Zawada
