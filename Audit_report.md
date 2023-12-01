# Dokument Audytu Bezpieczeństwa Aplikacji PyGoat
___
Wykonali:
- Gabriel Ćwiek
- Karol Benć
- Patryk Machoczek
- Piotr Kupczyk

Data wykonania: 01.12.2023

Wersja dokumentu: 1.0

Typ audytu: OWASP Top 10
___

## Spis treści
- [Podsumowanie wykonanych prac](#podsumowanie-wykonanych-prac)
- [Zakres Audytu](#zakres-audytu)
    - [Cel dokumentu](#cel-dokumentu)
    - [Wykonane czynności](#wykonane-czynności)
    - [Zestawienie statystyczne](#zestawienie-statystyczne)
    - [Aplikacja PyGOAT](#aplikacja-pygoat)
- [Metodologia](#metodologia)
    - [Kryterium oceny podatności](#kryterium-oceny-podatności)
    - [Klasyfikacja podatności](#klasyfikacja-podatności)
    - [Proces oceny podatności](#proces-oceny-podatności)
- [Testowane komponenty](#testowane-komponenty)
- [Podatności aplikacji](#podatnosc-aplikacji)

## Podsumowanie wykonanych prac
## Zakres Audytu
### Cel dokumentu
### Wykonane czynności
### Zestawienie statystyczne
### Aplikacja PyGOAT
PyGOAT to celowo podatna na ataki aplikacja stworzona w języku Python z wykorzystaniem framework'u Django. Może być ona używana do nauki zabezpieczania aplikacji internetowych. Aplikacja obejmuje wiele podatności z listy OWASP Top 10, która jest szeroko uznawaną listą najważniejszych zagrożeń bezpieczeństwa aplikacji webowych. Podatności są zaprojektowane tak, aby odzwierciedlały realne sytuacje, z którymi mogą spotkać się programiści, co czyni PyGOAT użytecznym narzędziem do nauki realnych umiejętności związanych z bezpieczeństwem aplikacji.
## Metodologia
W ramach audytu, każdy członek zespołu został przydzielony do specyficznych obszarów aplikacji, które następnie poddawane były szczegółowym testom pod kątem podatności na ataki. Metodyka testowania, technologie oraz wykorzystywane narzędzia były pozostawione do wyboru poszczególnym audytorom, co pozwalało na dostosowanie podejścia do ich indywidualnych preferencji i doświadczeń. Działania te były realizowane zgodnie z wyznaczonymi zasadami i na oddzielnych instancjach aplikacji, aby zapewnić, że każdy testowany komponent lub obszar działa w izolowanym, czystym środowisku, co wykluczało wpływ działań innych członków zespołu na jakość testów.

Każda znaleziona podatność była dokładnie analizowana i oceniana niezależnie przez osobę przeprowadzającą dane testy, zgodnie z ustalonymi kryteriami oceny podatności oraz klasyfikacją podatności opisaną w kolejnych sekcjach raportu z audytu. Dodatkowo, aby zapewnić transparentność i współpracę w zespole, każdy członek miał możliwość przeglądania znalezisk i dokumentacji przygotowanej przez inne osoby w grupie audytowej.

Pod koniec przeprowadzania audytów i testów aplikacji został sporządzony raport zawierający wszystkie znaleziska, oceny, i rekomendowane środki zaradcze.

### Kryterium oceny podatności
Podatności zostały sklasyfikowane w czterostopniowej skali opisującej zarówno istotność skutków ich wykorzystania, jak i łatwość ich realizacji. Opis każdego z poziomów został zawart w następnej sekcji "Klasyfikacja podatności". <strong>Istotność skutków</strong> opisuje stopień, w jakim wykorzystanie podatności może wpłynąć na system lub aplikacje. Bierze pod uwagę potencjalne konsekwencje, takie jak naruszenie danych, uszkodzenie systemu, lub wpływ na dostępność do usługi. Dodatkowo w ramach oceny istotności skutków należy ocenić zasięg wpływu podatności, np.: czy dotyczy ona pojedynczego komponentu czy całego systemu. <strong>Łatwość realizacji</strong> ocenia natomiast jakie narzędzia, umiejętności, dostępy lub czynniki zewnętrzne są wymagane od napastnika w celu efektywnego wykorzystania podatności.

### Klasyfikacja podatności
**High**

Wykorzystanie podatności umożliwia przejęcie przynajmniej częściowej kontroli nad serwerem lub aplikacją, co wiąże się z bezpośrednim i znaczącym ryzykiem naruszenia bezpieczeństwa. Takie zagrożenia mogą prowadzić do uszkodzenia systemu lub nieautoryzowanego dostępu do danych wrażliwych i poufnych. Podatności tego typu są zazwyczaj łatwe do wykorzystania, nie wymagają od sprawcy posiadania wyspecjalizowanych umiejętności i specjalnych narzędzi lub wystarczy ich minimalny zakres (np.: posiadanie konta użytkownika w systemie). Reakacja na tego typu zagrożenia powinna być natychmiastowa i priorytetowa. Należy szybko zastosować odpowiednie środki zaradcze, aby zapobiec potencjalnym atakom i zminimalizować ryzyko. Przykładami wykorzystania tych podatności mogą być ataki polegającen na wykonaniu zdalnego kodu czy przejęcie uprawnień administratora serwera.

**Medium**

Podatności tego typu mogą wymagać od napastnika posiadania zaawansowanych umiejętności lub spełnienia bardziej skomplikowanych warunków, takich jak nieświadoma współpraca członka organizacji, który udostępnia swoje dane poprzez kliknięcie w link phishingowy. Wykorzystanie takiego zagrożenia zwykle umożliwia dostęp jedynie do ograniczonej ilości danych, danych o mniejszej wadze strategicznej, lub pozwala na dostęp tylko części serwera lub aplikacji. Skutki wykorzystania tej podatności zazwyczaj mogą być kontrolowane i minimalizowane w stosunkowo prosty sposób. Pomimo, że zagrożenie nie jest krytyczne, jego potencjalne skutki wymagają uwagi i powinny być odpowiednio zarządzane. Przykładem takiej podatności może być niewystarczające szyfrowanie czy nieprzemyślane konfiguracje systemu.

**Low**

Podatności niskiego poziomu mają ograniczony wpływ na ogólne bezpieczeństwo lub wymaga spełnienia bardzo trudnych wymagań. Chociaż mogą nie stanowić bezpośredniego ryzyka dla systemu, powinny być monitorowane, aby zapobiec ewentualnym przyszłym problemom. Do tego typu zagrożeń można zaliczyć nieaktualne certyfikaty czy niewielkie luki w zabezpieczeniach, które nie są łatwe do wykorzystania.

**Info**

Zagrożenia informacyjne nie stanowią bezpośredniego ryzyka dla bezpieczeństwa, ale dostarczają wartościowych informacji o stanie zabezpieczeń i potencjalnych obszarach do ulepszeń.

### Proces oceny podatności
1. **Identyfikacja podatność**
2. **Analiza podatności**
3. **Ocena ryzyka i przypisanie kategorii**
4. **Identyfikacja rekomendacji naprawczych**
5. **Dokumentacja podatności**
## Testowane komponenty
## Podatności aplikacji
| Numer | Nazwa Podatności                                                       | Ryzyko | Lokalizacja                                                              | Audytor          |
|-------|------------------------------------------------------------------------|--------|--------------------------------------------------------------------------|------------------|
| 1     | Wykorzystanie przerwanego dostępu - zmiana parametrów pliku cookie     | High   | http://127.0.0.1:8000/broken_access_lab_1                                | Patryk Machoczek |
| 2     | Wykorzystanie przerwanego dostępu - zmiana parametrów nagłówka zapytania| High   | http://127.0.0.1:8000/broken_access_lab_2                                | Patryk Machoczek |
| 3     | Wykorzystanie przerwanego dostępu - forsowanie ścieżki plików           | High   | http://127.0.0.1:8000/broken_access_lab_3, http://127.0.0.1:8000/broken_access_controle/secret | Patryk Machoczek |
| 4     | Błąd kryptograficzny - niewystarczający algorytm hashujący | Medium | http://127.0.0.1:8000/cryptographic_failure/lab | Patryk Machoczek    |
| 5     | Błąd kryptograficzny - ręczna modyfikacja plików cookie    | High | http://127.0.0.1:8000/cryptographic_failure/lab3    | Patryk Machoczek    |
| 6     | SQL Injection | High | http://127.0.0.1:8000/injection_sql_lab      | Piotr Kupczyk    |
| 7     | Command Injection - Name Server Lookup | High | http://127.0.0.1:8000/cmd_lab      | Piotr Kupczyk    |
| 8     | Command Injection - Evaluate any expression | High | http://127.0.0.1:8000/cmd_lab2      | Piotr Kupczyk    |
| 9     | Server-Side Table Injection | High | http://127.0.0.1:8000/stti     | Piotr Kupczyk    |
| 10     | Security Misconfiguration                                                     | High | http://localhost:8000/sec_mis_lab                                                       | Gabriel Ćwiek    |
| 11    | [Nazwa Podatności]                                                     | [Przykład] | [`Przykład.py`]                                                          | [Lorem ipsum]    |
| 12   | [Nazwa Podatności]                                                     | [Przykład] | [`Przykład.py`]                                                          | [Lorem ipsum]    |

### Szczegółowe opisy podatności
#### [HIGH] Wykorzystanie przerwanego dostępu - zmiana parametrów pliku cookie

**Opis:**  
W aplikacji wykryto podatność na przerwanie dostępu z wykorzystaniem pliku Cookie. Wykorzystanie tej podatności pozwala na dostęp do aplikacji z uprawnieniami admina.

**Warunki niezbędne do wykorzystania podatności:**
- Dostęp do aplikacji,
- Konto użytkownika.

**Szczegóły techniczne (Proof of Concept):**

Dostęp do funkcji admina jest zapisany w pliku cookie. Po zalogowaniu jako przykładowy użytkownik `jack:jacktheripper`, wartość cookie admin wynosi 0.
Aby potwierdzić występowanie podatności, należy wykonać następujące kroki:
1. Zalogować się do aplikacji jako użytkownik.
2. Otworzyć narzędzia deweloperskie i zlokalizować plik cookie.  
   ![Widok pliku cookie w narzędziach deweloperskich](img/A1_lab1_1.png)
3. Zmienić wartość parametru "admin" z 0 na 1.  
   ![Zmiana wartości pliku cookie - wyświetlona treść widoczna tylko dla admina](img/A1_lab1_2.png)
4. Wartość dostępna tylko dla admina jest teraz widoczna dla zwykłego użytkownika - Secret Key.

**Uwagi:**  
Brak

**Lokalizacja:** http://127.0.0.1:8000/broken_access_lab_1

**Rekomendacje:**
- Unikaj przechowywania wrażliwych informacji, takich jak uprawnienia użytkownika, w plikach cookie. Zamiast tego, preferuj przechowywanie identyfikatorów sesji.
- Przechowuj informacje o sesji po stronie serwera, a nie klienta. To ogranicza ryzyko manipulacji wartościami przechowywanymi w plikach cookie.
- Szyfruj informacje przechowywane w plikach cookie, aby utrudnić ich przechwycenie i modyfikację.
- Upewnij się, że każda operacja, która wymaga uprawnień administratora, jest dodatkowo sprawdzana po stronie serwera.
- Ustaw krótki czas trwania sesji, co wymusza regularne logowanie użytkowników, ograniczając potencjalny czas ataku.

**Więcej informacji:**
- https://owasp.org/Top10/A01_2021-Broken_Access_Control/
- https://www.eccouncil.org/cybersecurity-exchange/web-application-hacking/broken-access-control-vulnerability/
___
#### [HIGH] Wykorzystanie przerwanego dostępu - zmiana parametrów nagłówka zapytania

**Opis:**  
W aplikacji wykryto podatność na przerwanie dostępu z wykorzystaniem zmiany parametrów  nagłówka zapytania. Wykorzystanie tej podatności pozwala na dostęp do aplikacji z uprawnieniami admina.

**Warunki niezbędne do wykorzystania podatności:**
- Dostęp do aplikacji,
- Konto użytkownika,
- BurpSuite lub inne narzędzie wspomagające testowanie oprogramowania

**Szczegóły techniczne (Proof of Concept):**
W kodzie strony zlokalizowano komentarz, który mówi że dostęp do funkcji admina jest determinowany poprzez używaną przeglądarkę.
![Kod strony internetowej aplikacji](img/A1_lab2_1.png) 
Korzystając z Burp Suite, można w momencie nawiązywania połączenia ze stroną zmienić wartości nagłówków zapytania.
Aby potwierdzić występowanie podatności, należy wykonać następujące kroki:
1. Włączyć BurpSuite i przejść do zakładki Proxy/Intercept
2. Zalogować się jako użytkownik
3. W BurpSuite zmienić wartość User-Agent z przeglądarki na pygoat_admin.
![BurpSuite Proxy Intercept - widok zapytania http](img/A1_lab2_2.png)
4. Wartość dostępna tylko dla admina jest teraz widoczna dla zwykłego użytkownika, który ma status Admin - Secret Key.
![Widok admina](img/A1_lab2_3.png)

**Uwagi:**  
Brak

**Lokalizacja:** http://127.0.0.1:8000/broken_access_lab_2

**Rekomendacje:**
- Wprowadź solidny system autoryzacji i uprawnień, który dokładnie kontroluje dostęp do różnych funkcji aplikacji na podstawie kont użytkowników.
- Nie polegaj jedynie na informacjach przesyłanych przez przeglądarkę w nagłówkach zapytań. Weryfikuj uprawnienia na poziomie serwera.
- Używaj unikatowych identyfikatorów sesji dla każdego użytkownika, a nie polegaj wyłącznie na informacjach dostarczanych przez przeglądarkę, takich jak User-Agent.
- Przeprowadzaj wszystkie ważne walidacje i kontrole bezpieczeństwa po stronie serwera, a nie polegaj na danych dostarczanych przez przeglądarkę.
- Dodaj dodatkowe zabezpieczenia, aby uniemożliwić zmianę User-Agent w nagłówku zapytania. Ogranicz dozwolone wartości lub skonfiguruj system, który monitoruje i reaguje na podejrzane zmiany.
- Nie pozostawiaj w kodzie komentarzy zawierających informacje o mechanizmach autoryzacji. Usuń wszelkie zbędne informacje, które mogą ułatwić atakującym zrozumienie systemu.
- Dodaj zabezpieczenia do warstwy proxy, aby uniemożliwić manipulacje nagłówkami zapytań. Ogranicz dostęp do narzędzi takich jak Burp Suite tylko do autoryzowanych użytkowników.

**Więcej informacji:**
- https://owasp.org/Top10/A01_2021-Broken_Access_Control/
- https://owasp.org/www-community/Broken_Access_Control
- https://portswigger.net/web-security/access-control
___
#### [HIGH] Wykorzystanie przerwanego dostępu - forsowanie ścieżki plików (bruteforce file path)

**Opis:**  
W aplikacji wykryto podatność na przerwanie dostępu z wykorzystaniem forsowania ścieżki plików w aplikacji. Wykorzystanie tej podatności pozwala na dostęp do stron, które powinny być dostępne tylko dla użytkowników z odpowiednimi uprawnieniami.

**Warunki niezbędne do wykorzystania podatności:**
- Dostęp do aplikacji,
- Narzędzia do przeprowadzania bruteforce, np. GoBuster lub Burp Suite

**Szczegóły techniczne (Proof of Concept):**
Analizując aplikację z uprawnieniami admina, zauważono, że przycisk SECRET prowadzi do zasobów znajdujących się na stronie http://127.0.0.1:8000/broken_access_controle/secret. Znając adres strony, użytkownik jest w stanie zobaczyć jej treść mimo braku posiadania uprawnień administratora.
![Napis SECRET prowadzi do zasobów z pozoru dostępnych tylko dla admina](img/A1_lab3_1.png)
Aby potwierdzić występowanie podatności, należy wykonać następujące kroki:
1. Zlokalizować gdzie znajdują się zaosby, które powinny mieć ograniczony dostęp, w tym wypadku http://127.0.0.1:8000/broken_access_controle/secret
![Zasoby dostępne tylko dla admina](img/A1_lab3_2.png)
2. Zalogować się jako zwykły użytkownik
![Widok użytkownika, brak przycisku SECRET](img/A1_lab3_3.png)
3. Wejść w adres strony z ukrytymi zasobami
![Strona z ukrytymi zasobami](img/A1_lab3_4.png)
4. Wartość dostępna tylko dla admina jest widoczna dla zwykłego użytkownika. Po zalogowaniu się jako John w oknie InCognito i wpisaniu adresu, widzimy Secret Keys.

**Uwagi:**  
Brak

**Lokalizacja:** http://127.0.0.1:8000/broken_access_lab_3, http://127.0.0.1:8000/broken_access_controle/secret

**Rekomendacje:**
- Upewnij się, że w Twojej aplikacji istnieje odpowiednia kontrola autoryzacji. Ogranicz dostęp do zasobów na podstawie roli i uprawnień użytkowników.
- Wykorzystaj mechanizmy autoryzacji wbudowane w framework lub biblioteki, aby zapewnić skuteczną kontrolę dostępu.
- Unikaj używania statycznych adresów URL dla zasobów o ograniczonym dostępie. Zastosuj dynamiczne i trudne do zgadnięcia identyfikatory zasobów.
- Wprowadź system monitorowania, który śledzi próby dostępu do chronionych zasobów. Monitoruj logi, aby wykrywać potencjalne ataki.
- Zastosuj mechanizmy ochrony przed atakami typu brute force, na przykład blokowanie konta po kilku nieudanych próbach logowania.

**Więcej informacji:**
- https://owasp.org/Top10/A01_2021-Broken_Access_Control/
- https://www.fortinet.com/resources/cyberglossary/brute-force-attack
- https://owasp.org/www-community/controls/Blocking_Brute_Force_Attacks
___
#### [MEDIUM] Błąd kryptograficzny - niewystarczający algorytm hashujący

**Opis:**  
W aplikacji wykryto podatność obejmującą błąd kryptograficzny. Wykorzystany został mechanizm hashujący MD5, który da się w łatwy sposób rozszyfrować. 

**Warunki niezbędne do wykorzystania podatności:**
- Dostęp do aplikacji,
- Przeprowadzenie SQL Injection i wydobycie danych o użytkowniku i jego zaszyfrowanym haśle,
- Narzędzie do identyfikacji algorytmu hashującego, np. https://hashes.com/en/tools/hash_identifier
- Narzędzie do roszyfrowywania algorytmu MD5, np. https://md5decrypt.net/en/#answer

**Szczegóły techniczne (Proof of Concept):**
Po zastosowaniu SQL Injection udało się uzyskać informacje na temat danych logowania admina: admin,c93ccd78b2076528346216b3b2f701e6. Zaszyfrowane hasło łatwo rozpoznać i uzyskać poprawną wartość, pozwalającą na zalogowanie się do systemu jako admin.

Aby potwierdzić występowanie podatności, należy wykonać następujące kroki:
1. Przeprowadzić SQL injection i uzyskać dane logowania admina
2. Zidentyfikować algorytm hashujący, np. w https://hashes.com/en/tools/hash_identifier
![Identyfikator algorytmów hashujących](img/A2_lab1_1.png)
3. Rozszyfrować zahashowane hasło, np. w https://md5decrypt.net/en/#answer bądź wyszukując w Google
![Rozszyfrowane hasło](img/A2_lab1_2.png)
4. Zalogować sie jako admin korzystając z roszyfrowanego hasła
![Pomyślne logowanie](img/A2_lab1_3.png)

**Uwagi:**  
- Szanse na wystąpienie wymienionej podatności maleją, jeśli aplikacja jest odpowiednio zabezpieczona przed SQl Injection.

**Lokalizacja:** http://127.0.0.1:8000/cryptographic_failure/lab

**Rekomendacje:**
- Stosuj parametryzowane zapytania SQL, które są dostępne w większości języków programowania. Unikaj bezpośredniego osadzania danych użytkownika w zapytaniach SQL.
- Unikaj używania algorytmów hashujących, które są uważane za słabe, takich jak MD5. Zamiast tego, zastosuj bardziej bezpieczne algorytmy, na przykład SHA-256 czy SHA-3.
- Implementuj silne zasady haseł, wymuszając długie i unikalne kombinacje znaków.
- Regularnie wymuszaj zmianę haseł i monitoruj ich siłę.

**Więcej informacji:**
- https://www.pentestpeople.com/blog-posts/owasp-top-ten-cryptographic-failures
- https://learn.snyk.io/lesson/insecure-hash/
___
#### [HIGH] Błąd kryptograficzny - ręczna modyfikacja plików cookie
**Opis:**  
W aplikacji wykryto podatność na błędy kryptograficzne. Pliki cookie determinujące typ dostępu użytkownika są przechowywane w sesji klienta, przez co można je modyfikować.

**Warunki niezbędne do wykorzystania podatności:**
- Dostęp do aplikacji,
- Konto użytkownika,
- Możliwe jest przeprowadzenie ataku bruteforce wykorzystując np. Burp Suite.

**Szczegóły techniczne (Proof of Concept):**
Podczas analizy plików cookies jako zalogowany użytkownik, zidentyfikowano wartość odpowiadającą za przyznanie dostępu admina.

Aby potwierdzić występowanie podatności, należy wykonać następujące kroki:
1. Zalogować się jako użytkownik
2. Zlokalizować plik cookie - jego wartość ma strukturę: Użytkownik|Znacznik czasu
3. Zmodyfikować nazwę użytkownika i wpisać zamiast niej prawdopodobny tag dla administratora, np. Admin/admin/administrator.
4. Po wpisaniu "admin" udało się uzyskać dostęp administratora.
![Widok admina](img/A2_lab3_1.png)

**Uwagi:**  
-  Tag administratora może zostać znaleziony przy pomocy ataku brute force, np. w Burp Suite 

**Lokalizacja:** http://127.0.0.1:8000/cryptographic_failure/lab3

**Rekomendacje:**
- Zmodyfikuj sposób przechowywania plików cookie, aby uniemożliwić ich modyfikację przez użytkowników. Zastosuj skomplikowane mechanizmy szyfrowania lub podpisu cyfrowego do plików cookie.
- Zamiast polegać wyłącznie na nazwie użytkownika i znaczniku czasu w plikach cookie, używaj unikalnych identyfikatorów sesji, które są trudniejsze do odgadnięcia. To może obejmować generowanie losowych ciągów znaków, które są trudne do przewidzenia.
- Implementuj system monitorowania aktywności użytkowników, aby wykrywać podejrzane aktywności, takie jak wielokrotne nieudane próby logowania czy podejrzane modyfikacje plików cookie.
- Wprowadź opóźnienia między próbami logowania i zablokuj dostęp na pewien czas po kilku nieudanych próbach. To ograniczy skuteczność ataków brute force.

**Więcej informacji:**
- https://owasp.org/Top10/A02_2021-Cryptographic_Failures/
- https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes
- https://www.pullrequest.com/blog/what-are-cryptographic-failures-and-how-to-prevent-giant-leaks/
___
#### [HIGH] SQL Injection

**Opis:** 

Aplikacja dopuszcza możliwość wykorzystania podatności na atak typu SQL Injection, który pozwala napastnikowi uzyskać dostęp do aplikacji poprzez zalogowanie się jako administrator, a tym samym na nieautoryzowany dostęp do danych poufnych lub danych wrażliwych jej użytkowników. Atak polega na "wstrzyknięciu" złośliwego kodu SQL do wejścia aplikacji (w tym wypadku formularza logowania), który jest następnie interpretowany i wykonany przez system zarządzania bazą danych. Podatność ta jest spowodowana brakiem mechanizmów odpowiedzialnych za weryfikowanie danych wejściowych użytkowników przed przekazaniem ich do bazy SQL.

![Zalogowanie jako administrator](img/A3_lab1_1.png) 

**Warunki niezbędne do wykorzystania podatności:**
 1. Aplikacja internetowa musi wykorzystywać dane wejściowe od użytkowników bezpośrednio w zapytaniach SQL.
 2. Mechanizmy odpowiedzialne za weryfikacje i walidacje danych wejściowych od użytkowników nie są zaimplementowane lub są zaimplementowane niepoprawnie.
 3. Napastnik, który chce użyć ataku SQL injection musi posiadać minimalną więdzę o działaniu baz danych typu SQL i posiadać uprawnienia wystarczające do wykonania zfałszowanego zapytania.

**Szczegóły techniczne (Proof of Concept):**
Przykładowe wykorzystanie podatności:
1. Napastnik wprowadza złośliwy fragment poleceniea SQL w pole 'password' formularza logowania, takie jak np.: "text_example' OR '1'='1"

![SQL injection](img/A3_lab1_2.png) 

2. Wejście to zakłóca logikę zamierzonego zapytania SQL i przekształca je z SELECT * FROM users WHERE username = 'admin' AND password = 'user_input' na SELECT * FROM users WHERE username = 'admin' AND password = 'user_input' OR '1'='1'
3. To zmienione zapytanie zawsze ewaluuje się jako prawdziwe ze względu na '1'='1', prowadząc do nieautoryzowanego dostępu do konta administratora

![SQL injection - pełne złościwe zapytanie](img/A3_lab1_3.png)

**Uwagi:**
Jest to podatność na bardzo popularny atak i powinna zostać naprawiona w trybie priorytetowym.

**Lokalizacja:**
Podatność jest możliwa do wykorzystania w aplikacji pod adresem: http://127.0.0.1:8000/injection_sql_lab. 
Jej przyczyna znajduje się w back-endzie aplikacji, gdzie przetwarzane są dane wejściowe użytkownika i wykonywane są zapytania SQL: "/static/templates/Lab/SQL/sql_lab.html".

**Rekomendacje:**
1. Używaj przygotowanych instrukcji z parametryzowanymi zapytaniami, aby zapobiec iniekcji SQL.
2. Wdrażaj walidację i weryfikacje danych wejściowych, aby upewnić się, że nie zawierają one złośliwego kodu SQL.
3. Regularnie audytuj i testuj aplikacje internetowe pod kątem podatności na iniekcje SQL.

**Więcej informacji:**
1. https://www.imperva.com/learn/application-security/sql-injection-sqli/
2. https://en.wikipedia.org/wiki/SQL_injection
3. https://www.w3schools.com/sql/sql_injection.asp
___
#### [HIGH] Command Injection - Name Server Lookup

**Opis:** 

Użytkownicy w aplikacji mają możliwość wyszukiwania serwera (name server lookup) dla podanej domeny. Należy podać nazwę domeny, po czym serwer przeprowadzi wyszukiwanie ns i zwróci wynik do klienta. Server look-up jest najprawdopodbniej wykonywany przy użyciu komendy: command="nslookup {}".format(domain), a zmienna komendy następnie przesyła się do funkcji exec. Użytkownik jednak przy okazji zmiennej serwera wprowadzić również dowolną komendą, która wykona się na danym serwerze, np.: gooogle.com && dir, gooogle.com && ls, google.com ; ipconfig itd. Z pomocą podatności udało się utworzyć nowy folder, odczytać pliki konfiguracyjne oraz usuwać wybraną zawartość nie posiadając żadnego dostępu do serwera. Dodatkowe dzięki tej podatności napastnik jest w stanie uzyskać nieautoryzowany dostęp do danych poufnych lub danych wrażliwych użytkowników aplikacji.

![Prawidłowe działanie funkcjonalności](img/A3_Lab2_1.png)

**Warunki niezbędne do wykorzystania podatności:**
Przykładowe wykorzystanie podatności:
1. Napastnik, który chce użyć ataku typu Command Injection musi posiadać minimalną więdzę o działaniu systemów operacyjnych i posiadać uprawnienia wystarczające do wykonania złośliwego kodu.
2. Mechanizmy odpowiedzialne za weryfikacje i walidacje danych wejściowych od użytkowników nie są zaimplementowane lub są zaimplementowane niepoprawnie.
3. Aplikacja posiada funkcjonalności, które wywoływują komendy systemowe bezpośrednio z punktów dostępu dla użytkowników końcowych.

**Szczegóły techniczne (Proof of Concept):** 
1. Napastnik wprowadza w pole "Enter Domain Here" dowolną domenę oraz fragment złośliwego kodu, który ma zostać wykonany na serwerze aplikacji, np.: "google.com && mkdir new_folder".

![Utworzenie nowego folderu na serwerze](img/A3_Lab2_2.png)
![Wywołanie prostej komendy ls - użytkownik dostaje listę plików serwera](img/A3_Lab2_3.png)

2. Server look-up jest wykonywany na serwerze przy użyciu komendy: command="nslookup {}".format(domain), a zmienna komendy następnie przesyła się do funkcji exec.
3. System wykona komende nslookup "domena", a następnie wykona złośliwy kod wprowadzony przez napastnika.

![Dowód na utworzenie nowego folderu na serwerze](img/A3_Lab2_4.png)

**Uwagi:**  
Jest to bardzo niebezpieczna podatność, która umożliwia napastnikowi na ingerencje w wenwnętrze pliki serwera, oraz dostęp do danych poufnych i danych wrażliwych użytkowników.

**Lokalizacja:**
Podatność jest możliwa do wykorzystania w aplikacji pod adresem: http://127.0.0.1:8000/cmd_lab
Jej przyczyna znajduje się w implementacji funkcjonalność "Name Server Lookup": "/static/templates/Lab/SQL/cmd_lab.html".

**Rekomendacje:**
1. Wdrażaj walidację i weryfikacje danych wejściowych, aby upewnić się, że nie zawierają one złośliwego kodu.
2. Nie wywołuj komend systemowych bezpośrednio z punktów dostępu dla użytkowników końcowych oraz nie dawaj takiej możliwości użytkownikom końcowym.
3. Poza standardowymi mechanizmami walidacyjnymi, zastosuj specjalną walidację przeciwko komendą lub znakom zakazanym.

**Więcej informacji:**
1. https://brightsec.com/blog/os-command-injection/#command-injection-protection
2. https://portswigger.net/web-security/os-command-injection
3. https://developers.redhat.com/articles/2023/03/29/4-essentials-prevent-os-command-injection-attacks
___
#### [HIGH] Command Injection - Evaluate any expression

**Opis:** 

Użytkownicy w aplikacji mają możliwość obliczania dowolnego równania matematycznego. Należy podać równanie, np.: 125+125+125, po czym serwer przeprowadzi odpowiednie kalkulacje i zwróci wynik do klienta. Funkcjonalność jest wykonywana przy użyciu kodu python i funkcji eval() na poziomie serwera. Oznacza to, że dowolny użytkownik poza działaniami matematycznymi może wykonać na serwerze dowolną funkcję dostępną w języku python. Mimo, iż napastnicy nie otrzymują informacji zwrotnej to podatność ta pozostawia im szerokie pole do potencjalnych ingerencji w pliki konfiguracyjne serwera oraz naruszenia jego integralności. W ramach testów aplikacja w plikach serwera udało się utworzyć folder new_test_folder, a następnie go usunąć.

![Prawidłowe działanie funkcjonalności](img/A3_Lab3_1.png)

**Warunki niezbędne do wykorzystania podatności:**
1. Napastnik, który chce użyć ataku typu Command Injection musi posiadać minimalną więdzę o działaniu systemów operacyjnych, podstawową wiedzę z zakresu używania języka programowania Python i posiadać uprawnienia wystarczające do wykonania złośliwego kodu.
2. Mechanizmy odpowiedzialne za weryfikacje i walidacje danych wejściowych od użytkowników nie są zaimplementowane lub są zaimplementowane niepoprawnie.
3. Aplikacja posiada funkcjonalności, która pozwala na wywołanie komendy systemowej bezpośrednio z punktów dostępu dla użytkowników końcowych.

**Szczegóły techniczne (Proof of Concept):**
W celu odtworzenia tej podatności: 
1. Napastnik wprowadza w pole "Evaluate any expression!" fragment złośliwego kodu, np.: os.system("rmdir index.html").

![Utworzenie nowego folder w plikach serwera](img/A3_Lab3_2.png)

![Usunięcie folderu z plików serwera](img/A3_Lab3_4.png)

2. Komenda języka python eval() jest wykonywana z argumentem przesłanym przez użytkownika, co powoduje wykonanie złośliwego kodu na serwerze.

![Dowód na utworzenie nowego folder w plikach serwera](img/A3_Lab3_3.png)

![Dowód usunięcia](img/A3_Lab3_5.png)

**Uwagi:**  
Jest to bardzo niebezpieczna podatność, która umożliwia napastnikowi na ingerencje w wenwnętrze pliki serwera, oraz dostęp do danych poufnych i danych wrażliwych użytkowników.

**Lokalizacja:**
Podatność jest możliwa do wykorzystania w aplikacji pod adresem: http://127.0.0.1:8000/cmd_lab2
Jej przyczyna znajduje się w implementacji funkcjonalność "Evaluate any expression": ""/static/templates/Lab/SQL/cmd_lab2.html""

**Rekomendacje:**
1. Wdrażaj walidację i weryfikacje danych wejściowych, aby upewnić się, że nie zawierają one złośliwego kodu.
2. Nie wywołuj komend systemowych bezpośrednio z punktów dostępu dla użytkowników końcowych.
3. Poza standardowymi mechanizmami walidacyjnymi, zastosuj specjalną walidację przeciwko komendą lub znakom zakazanym.

**Więcej informacji:**
1. https://brightsec.com/blog/os-command-injection/#command-injection-protection
2. https://portswigger.net/web-security/os-command-injection
3. https://developers.redhat.com/articles/2023/03/29/4-essentials-prevent-os-command-injection-attacks
___
#### [HIGH] Server-Side Table Injection

**Opis:**

Użytkownicy aplikacji są w stanie dodawać wpisy na blogu przez odpowiednio do tego przygotowany formularz. Wykorzystywany jest do tego standardowy szablon z frameworku języka Python - Django. Szablony pozwalają na dynamiczne generowanie kodu HTML, a tym samym treści aplikacji, na podstawie dostarczanych przez użytkownika danych. Silniki szablonów, odpowiedzialne za ich kompilacje, są w stanie uruchamiać pewne polecenia na maszynach wirtualnych / serwerach oraz uzyskiwać dostęp do zmiennych środowiskowych i lokalnych. Wprowadzone dane przez użytkownika nie są w żaden sposób walidowane, weryfikowane i filtrowane, co daje możliwość wprowadzenia złośliwego kodu / złośliwego oprogramowania, które pobierze pewne dane wrażliwe lub dane poufne i wyświetli je na stronie danego wpisu.

![Podstawowe działanie bloga](img/A3_Lab4_3.png)

**Warunki niezbędne do wykorzystania podatności:**
1. Niezwalidowane i niewyczyszczone dane użytkownika muszą być bezpośrednio osadzane w szablonach po stronie serwera.
2. Atakujący musi być w stanie wstrzyknąć złośliwe dyrektywy lub kod do szablonów. W tym celu musi posiadać podstawową wiedzę z zakresu silników szablonów Django.
3. Dane dostarczone przez użytkownika muszą być akceptowane przez aplikację bez przeprowadzenia odpowiedniej walidacji lub oczyszczania

**Szczegóły techniczne (Proof of Concept):**
Przykład wykorzystania podatności:
1. W formularzu "Add Blog" napastnik wpisuje komendę: {% load dowolny_tag %}, co prowadzi do wywołania błędu serwera i wyświetlenia listy dostępnych tagów. W tym momencie jesteśmy świadomi, że jesteśmy w stanie wykorzystac podatność typu Server-Side Table Injection.
![Uzyskanie dostępu do tagów](img/A3_Lab4_1.png)

![Spis tagów](img/A3_Lab4_2.png)

2. W formularzu "Add Blog" napastnik wpisuje skrypt, który z logów pobierze ostatnie 10 akcji wykonanych przez administratora i wyświetli jego zahashowane hasło.

![Skrypt, który wykorzystuje podatność](img/A3_Lab4_4.png)

![Efekt wykorzystania podatności](img/A3_Lab4_5.png)

**Uwagi:**  
Ta podatność jest bardzo niebezpieczna, ponieważ umożliwia atakującemu wykonywanie dowolnych poleceń systemowych na serwerze, co może prowadzić do utraty danych, naruszenia bezpieczeństwa i dostępu do poufnych informacji. Powinna zostać ona naprawiona w trybie priorytetowym.

**Lokalizacja:**
Podatność jest możliwa do wykorzystania w aplikacji pod adresem: http://127.0.0.1:8000/stti
Jej przyczyna znajduje się w implementacji funkcjonalność "Evaluate any expression": "/static/templates/Lab_2021/A3_injection/ssti_lab.html"

**Rekomendacje:**
1. Wdrażaj walidację i weryfikację danych wejściowych: Upewnij się, że dane dostarczane przez użytkowników są starannie walidowane i oczyszczone z potencjalnie niebezpiecznych znaków lub poleceń.
2. Unikaj wykonywania komend systemowych bezpośrednio z danych dostarczanych przez użytkownika: Nie używaj danych od użytkowników do tworzenia i wykonywania komend systemowych.
3. Zastosuj listę dozwolonych komend i parametrów.

**Więcej informacji:**
1. https://medium.com/@rupakbiswas2304/server-side-template-injection-8113cdbb2779
2. https://lifars.com/wp-content/uploads/2021/06/Django-Templates-Server-Side-Template-Injection-v1.0.pdf
3. https://github.com/Lifars/davdts
4. https://gitbook.seguranca-informatica.pt/fuzzing-and-web/server-side-template-injection-ssti
___
# [HIGH] Błędna konfiguracja zabezpieczeń

**Opis:**  
Wrażliwość pozwala na dostęp do Klucza projektu pozwalającego na enkrypcje i dekrypcje wiadomości

**Wymagania aby wykożystać lukę:**  
 - Konto użytkownika  
 - Dostęp do aplikacji  
 - Przeglądarka z możliwością edycji zapytań (w tym wypadfku FF Developer)

**Sczegółowy opis problemu:**  
Aplikacja umożliwia użytkownikowi z uprawnieniami administratora uzyskać dostęp do prywatnego klucza aplikacji, poprzez wysłana zapytania pod odpowiedni adres. Niestety sprawdza ona tylko nazwę hosta który ma obsłużyć żądanie, a nie sprawdza czy użytkownik jest autoryzowany do tego żądania.

**Wykożystanie podatności:**  
Podatność daje dostęp użytkownikowi dostęp do klucza prywatnego strony co może  mu umożliwić uzyskanie dostępu do poufnych informacji, takich jak hasła, dane bankowe, itp. przez rozszyfrowanie wiadomości innych użytkowników.

**Szczegóły techniczne:**  
Po zalogowaniu się użytkownik ma możliwość wysłania zapytania o klucz prywatny, przez naciśnięcie odpowiedniego przycisku. Po przetworzeniu żądania użytkownik zostaje wprost poinformowany o tym, który adres służy do przetwarzania tego wymagania i w którym polu je wstawić
![Widok użytkownika](img/A5-image.png)
Po edycji poprzedniego żądania, uzupełnieniu go w odpowiednie pole i wysłaniu ponownie uzyskujemy dostęp do klucza publicznego.  
![Edycja zapytania](img/A5-image-1.png)
![Uzyskany klucz](img/A5-image-3.png)

**Rekomendacje:**
1. Żaden użytkownik, ani administrator, który nie jest administratorem serwera nie powinien mieć dostępu do klucza prywatnego
2. Jeżeli powyższe nie jest możliwe to należy dodać autoryzacje i autentyfikacje użytkowników, wysyłających zapytania pod podany adres
3. Usunąć informację zwrotną podającą dokładny adres i przyczynę odrzucenia żądania
4. Brak odpowiednich zabezpieczeń w dowolnej części stosu aplikacji lub nieprawidłowo skonfigurowane uprawnienia w usługach w chmurze.  
5. Niepotrzebne funkcje są włączone lub zainstalowane (np. niepotrzebne porty, usługi, strony, konta lub uprawnienia).
6. Domyślne konta i ich hasła są nadal włączone i niezmienione.
7.  W przypadku zaktualizowanych systemów najnowsze funkcje zabezpieczeń są wyłączone lub nie są skonfigurowane w bezpieczny sposób.
8. Ustawienia zabezpieczeń w serwerach aplikacji, frameworkach aplikacji (np. Struts, Spring, ASP.NET), bibliotekach, bazach danych itp. nie są ustawione na bezpieczne wartości.
9. Serwer nie wysyła nagłówków lub dyrektyw bezpieczeństwa lub nie są one ustawione na bezpieczne wartości.
___
