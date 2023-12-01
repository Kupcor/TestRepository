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
