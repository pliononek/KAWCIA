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

| Provider | Model | Klucz API |
|---|---|---|
| Google Gemini | gemini-1.5-flash | [aistudio.google.com](https://aistudio.google.com) |
| OpenAI | gpt-4o-mini | [platform.openai.com](https://platform.openai.com) |
| DeepSeek | deepseek-chat | [platform.deepseek.com](https://platform.deepseek.com) | | nie działa scanowanie jedzenia |
| Anthropic Claude | claude-haiku-4-5 | [console.anthropic.com](https://console.anthropic.com) |

---

## 🔑 Jak uzyskać darmowy klucz API Gemini?

1. Wejdź na [aistudio.google.com](https://aistudio.google.com)
2. Zaloguj się kontem Google
3. Kliknij **"Get API key"** → **"Create API key"**
4. Skopiuj klucz i wklej go w ustawieniach aplikacji

> ⚠️ Nie udostępniaj nikomu swojego klucza API.

---

## 🚀 Jak uruchomić?

**Opcja 1 — Github pages (najprostsze)**

Wejdź na [https://pliononek.github.io/KAWCIA/) w Safari na iPhonie lub Chrome na Androidzie.

**Opcja 2 — Lokalnie**

```bash
git clone https://github.com/pliononek/KAWCIA.git
cd KAWCIA
# Otwórz index.html w przeglądarce
```

**Opcja 3 — Własny hosting**

Wrzuć plik `index.html` na dowolny statyczny hosting (Netlify, Vercel, GitHub Pages, Cloudflare Pages).

---

## 📱 Jak dodać do ekranu głównego?

### iOS (Safari)
1. Otwórz aplikację w Safari
2. Kliknij **Udostępnij** (ikona kwadratu ze strzałką)
3. Wybierz **Dodaj do ekranu początkowego**

### Android (Chrome)
1. Otwórz aplikację w Chrome
2. Kliknij trzy kropki → **Dodaj do ekranu głównego**

---

## 🛠️ Technologie

Czysty HTML + CSS + JavaScript w jednym pliku — zero frameworków, zero buildu, zero zależności.

- **HTML5 / CSS3 / Vanilla JS (ES6+)**
- **Web Storage API** (`localStorage`) — dane użytkownika
- **Web Crypto API** — bezpieczeństwo
- **Web Audio API** — dźwięk timera
- **ZXing** — skanowanie kodów kreskowych
- **Open Food Facts API** — baza produktów spożywczych
- **Canvas Confetti** — bo kończenie treningu zasługuje na świętowanie 🎉

---

## 📝 Licencja

Projekt ma dwie osobne licencje:

**Kod źródłowy — MIT**
Cały kod (`index.html`, `README.md` itd.) jest dostępny na licencji MIT. Możesz go dowolnie modyfikować, forkować i używać.

**Ikona aplikacji — All Rights Reserved ⚠️**
Zdjęcie użyte jako ikona aplikacji jest chronione prawem autorskim i nie podlega licencji MIT. Zabronione jest kopiowanie, redystrybucja, modyfikacja oraz użycie komercyjne bez pisemnej zgody autora.
