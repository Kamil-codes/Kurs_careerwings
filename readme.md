# Chatbot AI z analizą danych
Aplikacja webowa łącząca czat z Claude (Anthropic) z możliwością przesyłania i analizowania plików CSV oraz XLSX.
Model generuje narracyjne podsumowanie danych w formie czytelnego raportu HTML.
# Funkcje
- Czat z Claude z obsługą historii rozmowy
- Streszczanie tekstów
- Upload plików CSV i XLSX oraz automatyczna analiza z wykresem
- Generowanie raportów HTML
- System logowania (hasła hashowane przez bcrypt)
- Rate limiting chroniący przed nadużyciami
- Podstawowa ochrona przed prompt injection
- Możliwość pobierania i usuwania raportów
- Możliwość pobierania i usuwania historii rozmowy
# Wymagania
- Python 3.10 lub nowszy
- Konto na console.anthropic.com z kluczem API
# Instalacja lokalna
1. Sklonuj repozytorium:
```bash
git clone https://github.com/twoj-login/nazwa-repo.git
cd nazwa-repo
```
2. Stwórz i aktywuj wirtualne środowisko:
Windows:
```bash
Windows:
python -m venv venv
source venv/bin/activate

Linux/macOS:
python3 -m venv .venv
source .venv/bin/activate
```
3. Zainstaluj zależności:
```bash
pip install -r requirements.txt
```
4. Stwórz plik .env w głównym folderze i uzupełnij:
```
ANTHROPIC_API_KEY=twoj-klucz-tutaj
SECRET_KEY=dowolny-dlugi-losowy-tekst
```
5. Uruchom appkę:
```bash
python app.py
```
6. Otwórz w przeglądarce: http://127.0.0.1:8080
# Zmienne środowiskowe
| Nazwa | Opis | Wymagane |
| -| -| -|
| ANTHROPIC_API_KEY | Klucz API do Claude | Tak |
| SECRET_KEY | Sekret do podpisywania sesji Flaska | Tak |
| PORT | Port appki (ustawiane automatycznie przez platformę) | Nie |
# Struktura projektu
```
app.py                  główny plik aplikacji
templates/              szablony HTML (Jinja2)
static/                 pliki CSS i zasoby statyczne
users/                  dane użytkowników, rozmowy i raporty
requirements.txt        lista zależności Pythona
.gitignore              pliki pomijane przez Git
```

# Autor
Kamil/kamcode, projekt stworzony w ramach kursu.