# 🎒 Wychodzimy!

Checklista przed wyjściem z domu z dziećmi. Działa w przeglądarce Chrome jako aplikacja offline (PWA). Instalujesz ją przez Chrome — pojawia się na ekranie głównym telefonu jak normalna apka.

---

## ✅ Co robi aplikacja

- 120+ rzeczy w 10 kategoriach (jedzenie, higiena, ubrania, apteczka…)
- 12 gotowych zestawów wyjść (krótki spacer, lekarz, podróż autem, zima, lato…)
- Odhaczanie rzeczy jako spakowane
- Filtrowanie po kategorii lub zestawie
- Dodawanie własnych rzeczy
- Tryb ciemny
- Działa **całkowicie offline** po pierwszym wczytaniu
- Dane zapisują się lokalnie w telefonie

---

## 🚀 Jak uruchomić (GitHub Pages)

### Krok 1 — stwórz repozytorium na GitHubie

1. Wejdź na [github.com](https://github.com) → **New repository**
2. Nazwa: `wychodzimy` (lub dowolna)
3. Ustaw jako **Public** (GitHub Pages działa bezpłatnie tylko dla publicznych)
4. Kliknij **Create repository**

### Krok 2 — wrzuć pliki

Opcja A — przez interfejs GitHub (najprościej):
1. Wejdź w swoje nowe repo
2. Kliknij **Add file → Upload files**
3. Przeciągnij pliki: `index.html`, `manifest.json`, `sw.js`, `icon.svg`
4. Kliknij **Commit changes**

Opcja B — przez terminal:
```bash
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin https://github.com/TWÓJ_LOGIN/wychodzimy.git
git push -u origin main
```

### Krok 3 — włącz GitHub Pages

1. W repo wejdź w **Settings → Pages**
2. Source: **Deploy from branch**
3. Branch: **main**, folder: **/ (root)**
4. Kliknij **Save**
5. Za chwilę (1–2 min) pojawi się adres np.: `https://twójlogin.github.io/wychodzimy`

---

## 📱 Instalacja na telefonie (Chrome → skrót na ekranie)

1. Otwórz Chrome na Androidzie
2. Wejdź na swój adres GitHub Pages
3. Poczekaj aż strona się załaduje (pierwsze ładowanie potrzebuje internetu)
4. Kliknij **⋮ (trzy kropki)** w prawym górnym rogu Chrome
5. Wybierz **„Dodaj do ekranu głównego"** lub **„Zainstaluj aplikację"**
6. Kliknij **Dodaj**
7. Gotowe! Ikona 🎒 pojawi się na ekranie telefonu

Od teraz aplikacja działa offline — nie potrzebujesz internetu.

---

## 📂 Struktura plików

```
wychodzimy/
├── index.html    ← cała aplikacja (HTML + CSS + JS w jednym pliku)
├── manifest.json ← konfiguracja PWA (nazwa, ikona, kolory)
├── sw.js         ← service worker (cache offline)
├── icon.svg      ← ikona aplikacji
└── README.md     ← ten plik
```

---

## 🔧 Personalizacja

Wszystko jest w `index.html`. Żeby edytować:

- **Dodać rzecz na stałe do listy domyślnej** → znajdź tablicę `ITEMS_DEF` w sekcji `// DATA`
- **Dodać własny zestaw** → tablica `PRESETS`
- **Zmienić kolory** → zmienne CSS `:root { --accent: ... }`

---

## 📋 Roadmapa

- **v1.1** — wyszukiwarka, sortowanie, eksport JSON
- **v1.2** — widget na ekran telefonu
- **v1.3** — tryb pogodowy (zimno/deszcz/upał) bez internetu
- **v1.4** — tryb głosowy, profile dzieci

---

## 📄 Licencja

MIT — rób co chcesz, używaj, modyfikuj, dziel się.
