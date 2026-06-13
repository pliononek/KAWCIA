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

## 🤖 Obsługiwane modele AI

| Provider | Model | Skanowanie zdjęć |
|---|---|---|
| Google Gemini | gemini-2.5-flash | ✅ działa |
| OpenAI | gpt-4o-mini | ✅ działa |
| Anthropic Claude | claude-haiku-4-5 | ✅ działa |
| DeepSeek | deepseek-chat | ❌ nie obsługuje zdjęć |

> 💡 **Polecamy Google Gemini** — darmowy, szybki i obsługuje wszystkie funkcje w tym skanowanie zdjęć posiłków.

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

Wejdź na [https://pliononek.github.io/KAWCIA/](https://pliononek.github.io/KAWCIA/) — działa od razu, bez instalacji.

---

### 🛠️ Lokalnie (dla zaawansowanych)

```bash
git clone https://github.com/pliononek/KAWCIA.git
cd KAWCIA
# Otwórz plik index.html w przeglądarce (dwuklik)
```

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
