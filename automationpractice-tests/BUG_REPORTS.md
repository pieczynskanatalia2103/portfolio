# ZGŁOSZENIA BŁĘDÓW (BUG REPORTS) - AUTOMATIONPRACTICE.PL

**Projekt:** Testowanie portalu e-commerce AutomationPractice.pl  
**Data:** 17.01.2026  

---

## BUG-001: Niepoprawna treść komunikatu o istniejącym adresie e-mail 

**Status:** Nowy  
**Priorytet:** Niski

### Opis
Podczas próby założenia konta na istniejący adres e-mail system blokuje rejestrację, ale wyświetlany komunikat zawiera niepoprawną treść i niepotrzebny identyfikator "1." .

### Kroki do reprodukcji
1. Otwórz stronę główną
2. Kliknij „Sign in”
2. Wpisz istniejący email w sekcji „Create an account”
3. Kliknij „Create an account”

### Oczekiwany rezultat
Wyświetlany jest poprawny komunikat informujący o istniejącym koncie.
"Konto na ten adres e-mail zostało już zarejestrowane. Podaj inny adres e-mail"

### Rzeczywisty rezultat
Wyświetlany jest komunikat "1. Konto na ten adres e-mail zostało już zarejestrowane. Podaj prawidłowe hasło lub poproś o nowe." 

### Załączniki
- [screenshot](./screenshots/BUG-001.jpg)

---

## BUG-002: Niepoprawna treść komunikatu o wymaganych polach 

**Status:** Nowy
**Priorytet:** Niski

### Opis
Podczas próby rejestracji bez uzupełnienia wymaganych pól system wyświetla komunikat w mało czytelnym formacie. 

### Kroki do reprodukcji
1. Otwórz stronę główną
2. Kliknij „Sign in”
3. Wpisz poprawny email w sekcji „Create an account”
4. Kliknij „Create an account”
2. Nie uzupełniaj wszystkich wymaganych pól
3. Kliknij „Register”

### Oczekiwany rezultat
Wyświetlany jest poprawny komunikat informujący o wymaganych polach.
"Proszę uzupełnić wszystkie wymagane pola"

### Rzeczywisty rezultat
Wyświetlany jest komunikat "There are 3 errors
1. lastname is required.
2. firstname is required.
3. passwd is required."

### Załączniki
- [screenshot](./screenshots/BUG-002.jpg)

---




