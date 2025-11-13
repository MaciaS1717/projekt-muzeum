# Projekt Muzeum – Django (backend) + React (frontend)

To repozytorium zawiera środowisko do pracy zespołowej nad projektem muzeum, zbudowane przy użyciu Django (backend API) oraz React (frontend).
Projekt jest przygotowany do pracy w Visual Studio Code z użyciem wirtualnego środowiska Pythona (venv), bez Dockera.

---

## Wymagania

Upewnij się, że masz zainstalowane:

- Python 3.10+
- Node.js 18+
- Git
- Visual Studio Code
- Rozszerzenia VS Code:
  - Python (Microsoft)

---

## Klonowanie repozytorium z Bitbucket

W terminalu wykonaj:

```bash
git clone https://devtools.wi.pb.edu.pl/bitbucket/scm/pz2025muz/pz2025muz.git/
cd projekt-muzeum
```

Następnie otwórz katalog projektu w Visual Studio Code.

---

# Backend (Django)

## 1. Utworzenie i aktywacja wirtualnego środowiska venv

W głównym katalogu projektu:

```bash
python -m venv .venv
```

Aktywacja venv:

Windows (PowerShell):

```bash
.\.venv\Scripts\activate
```

Linux / Mac:

```bash
source .venv/bin/activate
```

---

## 2. Wybór interpretera Pythona w VS Code

1. Kliknij w lewym dolnym rogu VS Code na aktualnie wyświetlaną wersję Pythona.
2. Wybierz interpreter znajdujący się w katalogu `.venv`:
   - Windows: .venv/Scripts/python.exe
   - Linux/Mac: .venv/bin/python

---

## 3. Instalacja zależności backendu

```bash
pip install -r requirements.txt
```

---

## 4. Uruchomienie backendu

```bash
cd backend
python manage.py migrate
python manage.py runserver
```

Backend będzie działać pod adresem:

http://127.0.0.1:8000/

---

# Frontend (React)

## 1. Instalacja zależności

```bash
cd frontend
npm install
```

## 2. Uruchomienie frontendu

```bash
npm run dev
```

Frontend będzie działać pod adresem:

http://localhost:5173/

(właściwy port będzie wyświetlony w terminalu)

---

# Struktura projektu

```
projekt-muzeum/
├─ backend/        # Django backend (API)
├─ frontend/       # React frontend (UI)
├─ .venv/          # Wirtualne środowisko Pythona (lokalne)
├─ requirements.txt
├─ README.md
└─ .gitignore
```

---

# Praca zespołowa

- Główna gałąź: main
- Tworzenie nowych funkcjonalności: feature/nazwa-funkcji
- Aktualizacja projektu przed pracą: git pull origin main
- Wprowadzanie zmian przez Pull Requesty lub bezpośrednie commity zgodnie z ustalonym workflow

---

# Najważniejsze komendy Git

Pobranie najnowszych zmian:

```bash
git pull origin main
```

Dodanie zmian do commita:

```bash
git add .
```

Utworzenie commita:

```bash
git commit -m "Opis zmian"
```

Wysłanie zmian na Bitbucketa:

```bash
git push origin main
```

---

# Aktualizacja zależności backendu

Po instalacji nowych pakietów:

```bash
pip freeze > requirements.txt
```

Następnie commit i push do repozytorium.

---

# Uruchamianie projektu (podsumowanie)

Backend:

```bash
cd backend
python manage.py runserver
```

Frontend:

```bash
cd frontend
npm run dev
```

---
