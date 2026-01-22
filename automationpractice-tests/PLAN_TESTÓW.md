# PLAN TESTÓW - AUTOMATIONPRACTICE.PL

**Projekt:** Testowanie portalu e-commerce AutomationPractice.pl  
**Data:** 17.01.2026  
**Tester:** Natalia Pieczyńska  
**Wersja dokumentu:** 1.0

---

## 1. CEL TESTOWANIA

Weryfikacja funkcjonalności głównych modułów strony automationpractice.pl obejmujących:
- Proces rejestracji i logowania użytkownika
- Przeglądanie produktów i katalog
- Koszyk zakupów
- Proces dokonania zakupu
- Zarządzanie kontem użytkownika

---

## 2. ZAKRES TESTÓW

### Testowanie będzie obejmować:
- ✓ Testy funkcjonalne
- ✓ Testy interfejsu użytkownika (UI)
- ✓ Testy obsługi błędów
- ✓ Testy walidacji formularzy
- ✓ Testy responsywności (mobile, desktop)

### Poza zakresem testów:
- ✗ Testy wydajności (performance)
- ✗ Testy bezpieczeństwa (security)
- ✗ Testy obciążenia

---

## 3. ŚRODOWISKO TESTOWE

| Element | Opis |
|---------|------|
| **URL** | https://automationpractice.pl |
| **Przeglądarki** | Chrome, Firefox, Edge (wersje aktualne) |
| **System operacyjny** | Windows 11 | Android 13
| **Rozdzielczość ekranu** | 1920x1080, 1366x768 (mobile: 375x667) |
| **Połączenie internetowe** | Stabilne |

---

## 4. MODUŁY DO TESTOWANIA

### 4.1 Moduł Rejestracji i Logowania
- Rejestracja z poprawnymi danymi
- Rejestracja z niepoprawnymi danymi
- Logowanie z poprawnymi danymi
- Logowanie z niepoprawnymi danymi
- Wylogowanie użytkownika 

### 4.2 Moduł Produktów i Katalogu (testy automatyczne Cypress)
- Wyświetlanie listy produktów
- Filtrowanie produktów (kategoria, cena, ocena)
- Sortowanie produktów
- Wyszukiwanie produktów

### 4.3 Moduł Koszyka
- Dodawanie produktu do koszyka
- Usuwanie produktu z koszyka
- Zmiana ilości produktów
- Obliczanie sumowania ceny
- Ustalanie rabatów/kodów promocyjnych

### 4.4 Moduł Zamówienia
- Wybór adresu dostawy
- Wybór metody płatności
- Potwierdzenie zamówienia
- Przesłanie potwierdzenia zamówienia

### 4.5 Moduł Konta Użytkownika
- Wyświetlanie danych profilu
- Edycja danych osobowych
- Zarządzanie adresami dostawy
- Historia zamówień

---

## 5. KRYTERIA PRZEJŚCIA/NIEPRZEJŚCIA

### Przejście testu:
- ✓ Oczekiwany wynik zgodny z rzeczywistym
- ✓ Brak komunikatów o błędach
- ✓ Aplikacja odpowiada poprawnie w określonym czasie
- ✓ Interfejs wyświetla się prawidłowo

### Nieprzejście testu:
- ✗ Wynik rzeczywisty różni się od oczekiwanego
- ✗ Pojawienie się nieoczekiwanego błędu
- ✗ Aplikacja się zawiesza lub nie odpowiada
- ✗ Nieprawidłowe wyświetlanie interfejsu

---

## 6. HARMONOGRAM TESTÓW

| Faza | Zadanie |
|------|---------|
| **Faza 1** | Testowanie rejestracji i logowania 
| **Faza 2** | Testowanie katalogu produktów 
| **Faza 3** | Testowanie koszyka 
| **Faza 4** | Testowanie procesu zamówienia 
| **Faza 5** | Testowanie konta użytkownika


**Całkowity czas:** ~8 dni roboczych

---

## 7. TYPY TESTÓW

### Testy funkcjonalne
Weryfikacja poprawności funkcji i zachowania systemu

### Testy exploracyjne
Badanie aplikacji w poszukiwaniu nieoczekiwanych błędów

### Testy walidacji
Sprawdzenie walidacji danych wejściowych

---

## 8. REJESTRACJA I ZARZĄDZANIE BŁĘDAMI

Wszystkie znalezione błędy będą raportowane w formacie:
- **ID błędu: Tytuł**
- **Status**
- **Priorytet** 
- **Opis**
- **Kroki do reprodukcji**
- **Oczekiwany rezultat**
- **Rzeczywisty rezultat**
- **Załączniki**

---

## 9. WYMAGANE ARTEFAKTY TESTOWE

- [x] Plan testów (ten dokument)
- [x] Przypadki testowe (Test Cases)
- [x] Zgłoszenia błędów (Bug Reports)
- [] Raport z testów (Test Report)

---

**Dokument przygotowany jako część portfolio testerskiego.**
