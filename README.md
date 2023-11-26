# Dokument Audytu Bezpieczeństwa Aplikacji Python

## Spis treści
1. [Wstęp](#wstęp)
2. [Zakres Audytu](#zakres-audytu)
3. [Metodologia](#metodologia)
4. [Analiza Kodu Źródłowego](#analiza-kodu-źródłowego)
5. [Bezpieczeństwo Wewnętrzne](#bezpieczeństwo-wewnętrzne)
6. [Bezpieczeństwo Zewnętrzne](#bezpieczeństwo-zewnętrzne)
7. [Zarządzanie Dostępem i Uwierzytelnianie](#zarządzanie-dostępem-i-uwierzytelnianie)
8. [Testy Penetracyjne](#testy-penetracyjne)
9. [Rekomendacje](#rekomendacje)
10. [Podsumowanie](#podsumowanie)

## Wstęp
### Cel Dokumentu
### Zakres Dokumentu
### Definicje i Skróty


| ID | Nazwa Podatności | Poziom Ryzyka | Lokalizacja w Kodzie | Opis | Status Naprawy |
|----|------------------|---------------|----------------------|------|----------------|
| 1  | [Nazwa Podatności] | [Niski/Średni/Wysoki] | [np. `app/module.py:123`] | [Krótki opis] | [Niezałatwione/Załatwione] |
| 2  | [Nazwa Podatności] | [Niski/Średni/Wysoki] | [np. `app/views.py:45`] | [Krótki opis] | [Niezałatwione/Załatwione] |
| ... | ... | ... | ... | ... | ... |

#### ID 1
**medium**

| Nazwa podatności                | Kto robi?          | Status        |
|-------------------------------|------------------|---------------|
| Broken Access Control         | Patryk Machoczek  | DONE          |
| Cryptographic Failures        | Patryk Machoczek  | DONE          |
| SQL Injection                 | Piotr Kupczyk     | In progress   |
| Insecure Design               |                    | Not started   |
| Security Misconfiguration     |                    | Not started   |
| Components                    |                    | Not started   |
| Integrity Failures            |                    | Not started   |
| Server-Side Request Forgery   |                    | Not started   |
| Inne                          |                    | Not started   |

**High**
</br>
Wykorzystanie podatności umożliwia przejęcie przynajmniej częściowej kontroli nad serwerem lub aplikacją, co wiąże się z bezpośrednim i znaczącym ryzykiem naruszenia bezpieczeństwa. Takie zagrożenia mogą prowadzić do uszkodzenia systemu lub nieautoryzowanego dostępu do danych wrażliwych i poufnych. Podatności tego typu są zazwyczaj łatwe do wykorzystania, nie wymagają od sprawcy posiadania wyspecjalizowanych umiejętności i specjalnych narzędzi lub wystarczy ich minimalny zakres (np.: posiadanie konta użytkownika w systemie). Reakacja na tego typu zagrożenia powinna być natychmiastowa i priorytetowa. Należy szybko zastosować odpowiednie środki zaradcze, aby zapobiec potencjalnym atakom i zminimalizować ryzyko. Przykładami wykorzystania tych podatności mogą być ataki polegającen na wykonaniu zdalnego kodu czy przejęcie uprawnień administratora serwera.
</br>
**Medium**
</br>
Podatności tego typu mogą wymagać od napastnika posiadania zaawansowanych umiejętności lub spełnienia bardziej skomplikowanych warunków, takich jak nieświadoma współpraca członka organizacji, który udostępnia swoje dane poprzez kliknięcie w link phishingowy. Wykorzystanie takiego zagrożenia zwykle umożliwia dostęp jedynie do ograniczonej ilości danych, danych o mniejszej wadze strategicznej, lub pozwala na dostęp tylko części serwera lub aplikacji. Skutki wykorzystania tej podatności zazwyczaj mogą być kontrolowane i minimalizowane w stosunkowo prosty sposób. Pomimo, że zagrożenie nie jest krytyczne, jego potencjalne skutki wymagają uwagi i powinny być odpowiednio zarządzane. Przykładem takiej podatności może być niewystarczające szyfrowanie czy nieprzemyślane konfiguracje systemu.
</br>
**Low**
</br>
Podatności niskiego poziomu mają ograniczony wpływ na ogólne bezpieczeństwo lub wymaga spełnienia bardzo trudnych wymagań. Chociaż mogą nie stanowić bezpośredniego ryzyka dla systemu, powinny być monitorowane, aby zapobiec ewentualnym przyszłym problemom. Do tego typu zagrożeń można zaliczyć nieaktualne certyfikaty czy niewielkie luki w zabezpieczeniach, które nie są łatwe do wykorzystania.
</br>
**Info**
</br>
Zagrożenia informacyjne nie stanowią bezpośredniego ryzyka dla bezpieczeństwa, ale dostarczają wartościowych informacji o stanie zabezpieczeń i potencjalnych obszarach do ulepszeń.
