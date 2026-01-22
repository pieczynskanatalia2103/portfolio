## Test Cases
### Aplikacja: automationpractice.pl

## 1. Moduł rejestracji i logowania

### 1.1 Rejestracja użytkownika

#### TC-001 – Rejestracja z poprawnymi danymi
**Typ testu:** Pozytywny / Funkcjonalny
**Priorytet:** Wysoki

**Warunki wstępne:**
- Brak specjalnych warunków

**Dane testowe:**
- Email: test.user1@mail.com
- Hasło: Test123!
- Imię: Jan
- Nazwisko: Kowalski

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz poprawny email w sekcji "Create an account"
1. Kliknij "Create an account"
1. Uzupełnij wymagane pola formularza
1. Kliknij "Register"

**Oczekiwany rezultat:**
- Konto zostaje utworzone
- Użytkownik zostaje zalogowany
- Wyświetla się strona "My account"

**Wynik:** Zaliczony

---

#### TC-002 – Rejestracja z już istniejącym adresem email
**Typ testu:** Negatywny / Walidacja
**Priorytet:** Wysoki

**Warunki wstępne:**
- Brak specjalnych warunków

**Dane testowe:**
- Email: test@test.com

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz istniejący email w sekcji "Create an account"
1. Kliknij "Create an account"

**Oczekiwany rezultat:**
- Wyświetla się komunikat o istniejącym koncie
- Rejestracja nie jest możliwa

**Wynik:** Zaliczony

**Defekt:** BUG-001: Niepoprawna treść komunikatu o istniejącym adresie e-mail

---

#### TC-003 – Rejestracja bez wymaganych pól
**Typ testu:** Negatywny / Walidacja
**Priorytet:** Średni

**Warunki wstępne:**
- Brak specjalnych warunków

**Dane testowe:**
- Email: test.user2@mail.com
- Imię: (puste)
- Nazwisko: (puste)
- Hasło: (puste)

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz poprawny email w sekcji "Create an account"
1. Kliknij "Create an account"
1. Nie uzupełniaj wszystkich wymaganych pól
1. Kliknij "Register"

**Oczekiwany rezultat:**
- Formularz nie zostaje wysłany
- Wyświetlone są komunikaty walidacyjne

**Wynik:** Zaliczony

**Defekt:** BUG-002: Niepoprawna treść komunikatu o wymaganych polach

---

#### TC-004 – Rejestracja z niepoprawnym formatem email
**Typ testu:** Negatywny / Walidacja
**Priorytet:** Średni

**Warunki wstępne:**
- Użytkownik nie posiada konta

**Dane testowe:**
- Email: testmail.com

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz niepoprawny email w sekcji "Create an account"
1. Kliknij "Create an account"

**Oczekiwany rezultat:**
- Wyświetlany jest komunikat o niepoprawnym emailu

**Wynik:** Zaliczony

---

#### TC-005 – Rejestracja z hasłem niespełniającym wymagań
**Typ testu:** Negatywny / Bezpieczeństwo
**Priorytet:** Średni

**Warunki wstępne:**
- Użytkownik wpisał poprawny adres e-mail i przeszedł na stronę "Create an account"

**Dane testowe:**
- Email: test.user3@mail.com
- Imię: Jan
- Nazwisko: Kowalski
- Hasło: 123

**Kroki:**
1. Uzupełnij formularz rejestracji danymi testowymi
1. Kliknij "Register"

**Oczekiwany rezultat:**
- Rejestracja nie powiodła się
- Wyświetlany jest komunikat o wymaganiach hasła

**Wynik:** Zaliczony

---

### 1.2 Logowanie użytkownika

#### TC-006 – Logowanie z poprawnymi danymi
**Typ testu:** Pozytywny / Funkcjonalny
**Priorytet:** Wysoki

**Warunki wstępne:**
- Użytkownik posiada aktywne konto

**Dane testowe:**
- Email: test.user1@mail.com
- Hasło: Test123!

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz poprawny email i hasło w sekcji "Already registered?"
1. Kliknij "Sign in"

**Oczekiwany rezultat:**
- Użytkownik zostaje zalogowany
- Wyświetla się strona "My account"

**Wynik:** Zaliczony

---

#### TC-007 – Logowanie z niepoprawnym hasłem
**Typ testu:** Negatywny / Bezpieczeństwo
**Priorytet:** Wysoki

**Warunki wstępne:**
- Użytkownik posiada aktywne konto

**Dane testowe:**
- Email: test.user1@mail.com
- Hasło: WrongPass123

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz poprawny email oraz niepoprawne hasło w sekcji "Already registered?"
1. Kliknij "Sign in"

**Oczekiwany rezultat:**
- Logowanie nieudane
- Wyświetlany jest komunikat o błędnych danych

**Wynik:** Zaliczony

---

#### TC-008 – Logowanie z nieistniejącym kontem
**Typ testu:** Negatywny / Walidacja
**Priorytet:** Średni

**Warunki wstępne:**
- Brak specjalnych warunków

**Dane testowe:**
- Email: no.user@mail.com
- Hasło: Test123!

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz niezarejestrowany email oraz hasło w sekcji "Already registered?"
1. Kliknij "Sign in"

**Oczekiwany rezultat:**
- Logowanie nieudane
- Wyświetlany jest komunikat o błędnych danych

**Wynik:** Zaliczony

---

#### TC-009 – Logowanie bez podania hasła
**Typ testu:** Negatywny / Walidacja
**Priorytet:** Średni

**Warunki wstępne:**
- Użytkownik posiada aktywne konto

**Dane testowe:**
- Email: test.user1@mail.com
- Hasło: (puste)

**Kroki:**
1. Otwórz stronę główną
1. Kliknij "Sign in"
1. Wpisz zarejestrowany email w sekcji "Already registered?"
1. Kliknij "Sign in"

**Oczekiwany rezultat:**
- Logowanie nieudane
- Wyświetlany jest komunikat o wymogu podania hasła

**Wynik:** Zaliczony

---

#### TC-010 – Wylogowanie użytkownika
**Typ testu:** Pozytywny / Funkcjonalny
**Priorytet:** Średni

**Warunki wstępne:**
- Użytkownik jest zalogowany

**Kroki:**
1. Kliknij "Sign out"

**Oczekiwany rezultat:**
- Użytkownik zostaje wylogowany
- Wyświetla się strona logowania

**Wynik:** Zaliczony

## 2. Moduł Produktów i Katalogu (testy automatyczne Cypress)

## 3. Moduł koszyka (do automatyzacji)

### 3.1 Dodawanie, usuwanie zmiana

#### TC-011 – Dodawanie produktu do koszyka 
**Typ testu:**  Funkcjonalny
**Priorytet:**  Wysoki

**Warunki wstępne:**  
- Brak specjalnych warunków

**Kroki:**
1. Otwórz stronę główną
1. W polu wyszukiwania wpisz "Printed Chiffon Dress"
1. Kliknij enter lub ikonę lupy
1. Najedź na znaleziony przedmiot
1. Kliknij na zdjęcie
1. W rozwijanej liście Size wybierz "L"
1. Kliknij "Add to cart"

**Oczekiwany rezultat:**  
- pordukt został dodany do koszyka
- wyświetla się komunikat "Product successfully added to your shopping cart"

**Wynik**  
- Zaliczony

---



