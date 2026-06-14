# ☕ KAWCIA – Twój Osobisty Asystent Diety i Treningu

**KAWCIA** to nowoczesna, lekka i w pełni lokalna aplikacja webowa (PWA) stworzona z myślą o urządzeniach mobilnych. Pozwala na wygodne śledzenie spożytych kalorii, makroskładników oraz zrealizowanych planów treningowych.

Aplikacja stawia na **prywatność** – wszystkie Twoje dane są zapisywane wyłącznie na Twoim urządzeniu, żadne dane nie trafiają na serwer.

---

## ✨ Funkcje

- **📊 Licznik kalorii i makroskładników** — monitoruj spożycie kcal oraz białko, węglowodany i tłuszcze z czytelnym wskaźnikiem postępu
- **🤖 Analiza AI** — dodaj posiłek przez opis tekstowy, zdjęcie lub skan kodu kreskowego, a AI oszacuje kalorie i makro
- **🏋️ Moduł treningowy** — twórz treningi, dodawaj ćwiczenia, serie i powtórzenia, śledź rekordy osobiste (PR)
- **📚 Baza 60+ ćwiczeń** — wyszukiwarka z filtrami grup mięśniowych, możliwość dodania własnych ćwiczeń
- **⏱️ Timer przerw** — odlicza czas odpoczynku między seriami z powiadomieniem dźwiękowym i wibracjami
- **🎨 Motywy kolorystyczne** — fioletowy, niebieski lub pomarańczowy
- **📱 PWA** — działa jak natywna aplikacja po dodaniu do ekranu głównego
- **🔒 Privacy-First** — zero konta, zero serwera, dane tylko w `localStorage`

---

## 🤖 Modele AI (Google Gemini)

Aplikacja używa **Google Gemini** jako dostawcy AI. Klucz API jest darmowy.

| Model | RPM | RPD | Zdjęcia |
|---|---|---|---|
| gemini-3.1-flash-lite ⭐ | 15 | 500 | ✅ |
| gemini-2.5-flash | 5 | 20 | ✅ |
| gemini-2.5-flash-lite | 10 | 20 | ✅ |

> ❗nie dodawałem gpt ani antropic ponieważ za dużo błędów było z nimi a gemini api jest darmowe wiec dla przeciętnego użytkownika to wystarczy

> 💡 Aplikacja automatycznie zaczyna od **gemini-3.1-flash-lite** — najszybszy i najwięcej darmowych zapytań dziennie (500/dzień).

---

## 🔑 Krok po kroku: jak zdobyć darmowy klucz API Gemini

> Bez klucza API aplikacja nie będzie mogła analizować posiłków. Zajmuje to **2 minuty** i jest całkowicie darmowe.

**Krok 1** — Wejdź na stronę 👉 [aistudio.google.com](https://aistudio.google.com)

**Krok 2** — Kliknij **"Sign in"** i zaloguj się swoim kontem Google (tym samym co Gmail)

**Krok 3** — Po zalogowaniu kliknij niebieski przycisk **"Get API key"** w lewym górnym rogu

**Krok 4** — Kliknij **"Create API key"** → wybierz **"Create API key in new project"**

**Krok 5** — Pojawi się długi ciąg znaków (np. `AIzaSy...`). Kliknij ikonkę kopiowania obok niego.

**Krok 6** — Otwórz KAWCIA → wejdź w **Ustawienia** → wklej klucz w pole **"Klucz API Gemini"** → zapisz

> ⚠️ Klucz to jak hasło — nie pokazuj go nikomu i nie wklejaj na publicznych stronach.

---

## 🚀 Instalacja — krok po kroku

### 📱 iPhone (Safari)

**Krok 1** — Otwórz Safari i wejdź na:
```
https://pliononek.github.io/KAWCIA/
```

**Krok 2** — Na dole ekranu kliknij ikonkę **Udostępnij** (kwadrat ze strzałką skierowaną w górę ↑)

**Krok 3** — Przewiń listę w dół i kliknij **"Dodaj do ekranu początkowego"**

**Krok 4** — Kliknij **"Dodaj"** w prawym górnym rogu

**Krok 5** — Na pulpicie pojawi się ikona KAWCIA ☕ — otwieraj ją jak normalną aplikację!

> ⚠️ Używaj **Safari** — tylko Safari na iOS obsługuje dodawanie PWA do ekranu głównego. Chrome i Firefox na iPhonie tego nie umożliwiają.

---

### 🤖 Android (Chrome)

**Krok 1** — Otwórz Chrome i wejdź na:
```
https://pliononek.github.io/KAWCIA/
```

**Krok 2** — Kliknij trzy kropki ⋮ w prawym górnym rogu

**Krok 3** — Wybierz **"Dodaj do ekranu głównego"** lub **"Zainstaluj aplikację"**

**Krok 4** — Kliknij **"Dodaj"** — gotowe!

---

### 💻 Komputer (przeglądarka)

Wejdź na [https://pliononek.github.io/KAWCIA/) — działa od razu, bez instalacji.

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
# Python (wbudowany w macOS)
cd /ścieżka/do/folderu/z/index.html
python3 -m http.server 8080
# Wejdź na http://localhost:8080

# lub nginx przez Homebrew
brew install nginx
cp index.html /opt/homebrew/var/www/index.html
brew services start nginx
```

---

### 🌐 Udostępnienie przez internet (opcjonalne)

1. Sprawdź swoje publiczne IP: `curl ifconfig.me`
2. W routerze ustaw **port forwarding**: port `80` → Twój lokalny IP
3. Darmowa domena: [duckdns.org](https://duckdns.org)
4. HTTPS (wymagane do kamery w Safari): [certbot.eff.org](https://certbot.eff.org)

> ⚠️ Kamera działa tylko przez HTTPS lub `localhost`. Przez zwykłe HTTP Safari zablokuje dostęp do kamery.

---

## 🛠️ Technologie

Czysty HTML + CSS + JavaScript w jednym pliku — zero frameworków, zero buildu, zero zależności.

- **HTML5 / CSS3 / Vanilla JS (ES6+)**
- **Web Storage API** (`localStorage`) — dane użytkownika
- **Web Audio API** — dźwięk timera
- **ZXing** — skanowanie kodów kreskowych
- **Open Food Facts API** — baza produktów spożywczych
- **Canvas Confetti** — bo kończenie treningu zasługuje na świętowanie 🎉

---

## 📝 Licencja

**Kod źródłowy — MIT**
Cały kod (`index.html`, `README.md` itd.) jest dostępny na licencji MIT. Możesz go dowolnie modyfikować, forkować i używać.

**Ikona aplikacji — All Rights Reserved ⚠️**
Zdjęcie użyte jako ikona aplikacji jest chronione prawem autorskim i nie podlega licencji MIT. Zabronione jest kopiowanie, redystrybucja, modyfikacja oraz użycie komercyjne bez pisemnej zgody autora.
