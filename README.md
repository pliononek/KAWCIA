# ☕ KAWCIA – Twój Osobisty Asystent Diety i Treningu

**KAWCIA** to nowoczesna, lekka i w pełni lokalna aplikacja webowa (Single Page Application) stworzona z myślą o urządzeniach mobilnych i desktopowych. Pozwala na wygodne śledzenie spożytych kalorii, makroskładników, wypitej wody, masy ciała oraz zrealizowanych planów treningowych.

Aplikacja stawia na **prywatność (Privacy-First)** oraz **prostotę działania** – wszystkie Twoje dane są zapisywane wyłącznie na Twoim urządzeniu.

---

## ✨ Kluczowe funkcje

* **📊 Zaawansowany licznik kalorii i makroskładników:** Monitoruj spożycie kilokalorii (kcal) oraz podział na białka, węglowodany i tłuszcze w czasie rzeczywistym z czytelnym wskaźnikiem postępu.
* **🏋️ Rejestr i kreator treningów:** Twórz własne plany treningowe, dodawaj ćwiczenia, serie oraz powtórzenia. Aplikacja posiada wbudowany stoper/timer do odmierzania czasu przerw i świętuje Twój sukces efektownym confetti po ukończeniu sesji!
* **🔐 Prywatność i brak serwerów (Local-First):** Nie musisz zakładać konta ani się logować. Wszystkie dane są przechowywane w bezpieczny sposób bezpośrednio w pamięci podręcznej Twojej przeglądarki (`localStorage`).
* **📱 Projekt Mobile-First i PWA:** Aplikacja została zoptymalizowana pod kątem smartfonów. Posiada konfigurację `viewport-fit=cover`, ikony Apple Touch Icon oraz minimalistyczny, nowoczesny interfejs przypominający aplikację natywną.
* **🌙 Ciemny motyw (Dark Mode):** Stylowy, głęboki, mroczny interfejs oszczędzający baterię i wzrok podczas wieczornych wpisów.

---

## 🛠️ Technologie

Projekt został stworzony w oparciu o czyste, nowoczesne technologie webowe, co zapewnia błyskawiczne ładowanie i brak zbędnych zależności (no-build setup):

* **HTML5** (Semantyczna struktura, konfiguracja pod urządzenia Apple/PWA)
* **CSS3 / Modern UI** (Responsywny układ, płynne animacje, zmienne CSS do obsługi motywów)
* **Vanilla JavaScript (ES6+)** (Dynamiczne zarządzanie stanem aplikacji, obsługa zdarzeń i logika biznesowa)
* **Web Storage API (`localStorage`)** (Trwałe przechowywanie danych użytkownika bez bazy danych)
* **Canvas Confetti** (Zewnętrzna biblioteka skryptowa dodająca element grywalizacji po skończonym treningu)

---

## 🚀 Jak uruchomić projekt?

Aplikacja nie wymaga żadnej instalacji, kompilacji ani serwera Node.js. Jest w pełni samowystarczalna.

### Uruchomienie lokalne

1. Sklonuj to repozytorium:
   ```bash
   git clone https://github.com/TWOJ-USER/KOD-REPOZYTORIUM.git
   ```
2. Przejdź do katalogu projektu.
3. Otwórz plik `index.html` w przeglądarce (np. dwukliknij albo użyj prostego serwera HTTP: `python3 -m http.server`).

---

## 📱 Jak dodać aplikację na ekran główny telefonu?

Dzięki dostosowaniu do standardów aplikacji mobilnych, możesz korzystać z niej jak ze zwykłej aplikacji ze sklepu App Store / Google Play:

### iOS (Safari)

1. Otwórz stronę z aplikacją w przeglądarce Safari.
2. Kliknij przycisk **Udostępnij** (ikona kwadratu ze strzałką w górę).
3. Wybierz opcję **Dodaj do ekranu początkowego**.

### Android (Chrome)

1. Otwórz stronę w przeglądarce Chrome.
2. Kliknij ikonę trzech kropek w prawym górnym rogu.
3. Wybierz **Dodaj do ekranu głównego** lub **Zainstaluj aplikację**.

---

## 📝 Licencja

Projekt ma **dwie osobne licencje** — patrz pełny tekst w pliku [`LICENSE`](./LICENSE):

### 1. Kod źródłowy — MIT
Cały kod (`index.html`, `README.md`, itd.) jest udostępniony na licencji **MIT**.
Możesz go dowolnie modyfikować, forkować i używać do własnych potrzeb,
również komercyjnie.

### 2. Ikona aplikacji (zdjęcie twarzy) — All Rights Reserved ⚠️

Zdjęcie przedstawiające twarz autora, osadzone w `index.html` jako
`apple-touch-icon`, `<link rel="icon">` oraz w manifest PWA,
jest **chronione prawem autorskim** i NIE podlega licencji MIT.

**Zabronione bez pisemnej zgody autora:**
- kopiowanie i redystrybucja Ikony (również w forkach publikowanych
  na GitHubie, GitLabie itd.),
- używanie jako awatara, logo, znaku marki własnej lub cudzej,
- modyfikacja, retusz, deepfake, trening modeli AI na bazie Ikony,
- użycie komercyjne, reklamowe lub satyryczne.

**Przed publikacją własnego forka MUSISZ podmienić Ikonę na własną grafikę.**

Naruszenia podlegają ochronie zgodnie z ustawą o prawie autorskim
i prawach pokrewnych (Dz.U. 1994 Nr 24 poz. 83) oraz przepisami
międzynarodowymi.
