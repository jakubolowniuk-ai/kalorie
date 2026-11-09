# Kalorie

Prosty licznik kalorii i makroskładników na telefon (PWA). Działa w przeglądarce, dane są zapisane tylko w telefonie, kosztuje 0 zł.

## Pliki w repozytorium

| Plik | Co robi |
|---|---|
| `index.html` | Cała aplikacja: wygląd i logika |
| `sw.js` | Service worker, pozwala otworzyć aplikację bez internetu |
| `manifest.json` | Nazwa, kolory i ikona przy instalacji na ekranie głównym |
| `icon.svg`, `icon-192.png`, `icon-512.png` | Ikony aplikacji |
| `README.md` | Ta instrukcja |

---

## Publikacja na GitHub Pages (krok po kroku, z telefonu)

Wszystko da się zrobić w Chrome na Androidzie. Jeśli strona GitHuba wygląda dziwnie, w menu Chrome (⋮) zaznacz **„Wersja na komputer”**.

### 1. Załóż konto
1. Wejdź na **github.com** → **Sign up**.
2. Podaj e-mail, hasło i nazwę użytkownika (np. `jakub-kalorie`). Nazwa będzie częścią adresu aplikacji.
3. Potwierdź e-mail kodem, który przyjdzie na skrzynkę.

### 2. Utwórz repozytorium
1. Kliknij **+** (prawy górny róg) → **New repository**.
2. **Repository name:** `kalorie`
3. Zaznacz **Public** (darmowe GitHub Pages działa tylko dla publicznych repozytoriów; Twoje dane i tak zostają w telefonie, publiczny jest tylko kod).
4. Kliknij **Create repository**.

### 3. Wgraj pliki
1. Pobierz wszystkie 7 plików z czatu na telefon (trafią do folderu *Pobrane*).
2. W nowym repozytorium kliknij link **uploading an existing file** (albo **Add file → Upload files**).
3. Kliknij **choose your files** i zaznacz wszystkie pliki naraz.
4. Sprawdź, czy nazwy są dokładnie takie jak w tabeli powyżej. Telefon czasem dopisuje `(1)` do nazwy, wtedy aplikacja nie zadziała.
5. Na dole kliknij **Commit changes**.

### 4. Włącz GitHub Pages
1. W repozytorium wejdź w **Settings** (zakładka u góry).
2. Z menu po lewej wybierz **Pages**.
3. W sekcji **Build and deployment**:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`, folder `/ (root)` → **Save**.
4. Odczekaj 1–2 minuty i odśwież stronę. Pojawi się adres:
   `https://TWOJA-NAZWA.github.io/kalorie/`

### 5. Zainstaluj na telefonie
1. Otwórz ten adres w **Chrome**.
2. Menu **⋮** → **Dodaj do ekranu głównego** → **Zainstaluj**.
3. Ikona „Kalorie” pojawi się obok innych aplikacji. Od teraz otwieraj ją stamtąd.
4. Przy pierwszym skanowaniu kodu kreskowego zezwól na dostęp do aparatu.

---

## Aktualizacja aplikacji

1. Wejdź w repozytorium → kliknij plik, np. `index.html`.
2. Ikona ołówka ✏️ (edycja) lub **Add file → Upload files**, aby nadpisać plik nową wersją.
3. **Commit changes**.
4. Po 1–2 minutach zamknij aplikację w telefonie i otwórz ją ponownie (czasem trzeba dwa razy, bo telefon najpierw pokazuje zapamiętaną wersję).

Twoje dane (dziennik, produkty) **nie znikają** przy aktualizacji, bo są w telefonie, a nie na GitHubie.

---

## Jak korzystać

- **Dodawanie:** `+ Dodaj` przy posiłku → wpisz nazwę lub 📷 zeskanuj kod → wybierz produkt → jednostka i ilość → `Dodaj`.
- **Jednostki:** g/ml, opakowanie, porcja, sztuka, łyżka, łyżeczka, szklanka, plasterek, kromka, garść. Waga jednostki zależy od produktu, zmienisz ją w `Edytuj produkt`.
- **Własny produkt:** `+ Dodaj własny produkt` → formularz z etykiety. Produkty oznaczone ✓ to Twoje, sprawdzone.
- **⚠ Ostrzeżenie:** kalorie nie zgadzają się z makroskładnikami. Sprawdź etykietę i popraw produkt.
- **Edycja wpisu:** kliknij pozycję w dzienniku.
- **Kopiuj z wczoraj:** przycisk przy pustym posiłku.
- **Ustawienia ⚙:** cel kcal (domyślnie 1450), makro, motyw jasny/ciemny.

## Kopia zapasowa (ważne!)

Dane są tylko w przeglądarce telefonu. Wyczyszczenie danych Chrome lub zmiana telefonu = utrata danych.

- **Raz w tygodniu:** ⚙ → **Eksportuj** → zapisz plik `kalorie-kopia-RRRR-MM-DD.json` np. na Dysku Google.
- **Przywracanie:** ⚙ → **Importuj** → wybierz plik kopii.

## Źródła danych

- **Open Food Facts** (darmowa, otwarta baza, filtr: produkty sprzedawane w Polsce). Dane wpisują użytkownicy, więc mogą zawierać błędy, dlatego warto poprawiać produkty, z których często korzystasz.
- Około 25 produktów podstawowych wbudowanych w aplikację (wartości orientacyjne).
- Twoje własne produkty, zapisane lokalnie.

## Gdy coś nie działa

| Problem | Co sprawdzić |
|---|---|
| Strona pokazuje błąd 404 | Odczekaj 2 minuty; sprawdź, czy plik nazywa się dokładnie `index.html` |
| Brak opcji „Zainstaluj” | Czy w repozytorium są `manifest.json`, `sw.js` i obie ikony PNG? |
| Skaner nie działa | Zezwól na aparat (ikona kłódki przy adresie → Uprawnienia) |
| „Brak połączenia z Open Food Facts” | Brak internetu albo baza chwilowo nie odpowiada; własne i podstawowe produkty działają dalej |
| Nie widać nowej wersji | Zamknij i otwórz aplikację ponownie, ewentualnie dwa razy |
