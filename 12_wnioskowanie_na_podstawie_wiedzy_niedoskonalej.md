# Wnioskowanie na podstawie wiedzy niedoskonałej

Źródła niepewności wnioskowania:
- **niedoskonałość wiedzy**
- **niedoskonałość apratu pojęciowego**

## 1) Wnioskowanie i sieci bayesowskie

Gdy wiedza jest niedoskonała, czyli niepewność wobec wiedzy.

**Prawdopodobieństwo a priori** - bez znajomości obserwacji

**Prawdopodobieństwo warunkowe** - prawdopodobieństwo wystąpienia obserwacji, pod warunkiem hipotezy

**Prawdopodobieństwo a posteriori** - prawdopodbienstwo hipotezy przy założeniu obserwacji

Wzór:

>a posteriori(k) = (a priori(k) * warunkowe(k))/ suma(a priori(i) * warunkowe(i))

gdzie i dotyczy wszystkich hipotez, a k tych, których prawdopodobieństwo chcemy obliczyć

Model Bayesa pozwala obliczyć, jakie jest prawdopodobieństwo, że dana hipoteza jest prawdziwa w świetle przeprowadzonych obserwacj, dostępnych w bazie wiedzy faktów.

We wnioskowaniu probablistycznym dziedzinę problemu opisuje się za pomocą zbioru **zmiennych losowych**. Dla zmiennych losowych określa się **rozkład**, który określa z jakim prawdopodobieństwem przyjmuje ona poszczególne wartości. W ogólnym przypadku, gdy mamy do czynienia z n zmiennymi losowymi tworzą one **wektor losowy**, dla których określa się **rozkład wektora losowego**, nazywany często **rozkładem łącznym** (str. 181 rys. 12.1) Dla dwóch zmiennych losowych rozkład to tablica.

### Sieć bayesowska

**Sieć bayeseowska** jest skierowanym grafem acyklicznym wierzchołki to zmienne losowe a krawędzie to bezpośrednie zależności pomiędzy zmiennymi (jedno zależy od drugiego). Jeżeli X1(przyczyna) wskazuje na X2(skutek), to X1 jest poprzednikiem.( przykładowa sieć str. 184 rys. 12.2, a opis na 185-186)

DOCZYTAĆ!!

## 2) Teoria Dempstera-Shafera

Pomaga nam w wyrażaniu problemu braku wiedzy.

**Teoria Dempstera-Shafera, teria funkcji przekonania, matematyczna teoria ewidencji** - wyznacza prawdopodobieństwo z jakim dostępne informacje wspierają nasze przekonanie o prawdziwości danego twierdzenia, mierzone jest to za pomocą **funkcji przekonania**. Funkcja przekonani pełni również rolę *dolnego prawdopodobieństwa*, gdy *funkcja domniemania* pełnii rolę górnego prawdopodobieństwa.

W teorii dempstera shaffera przypisujemy stwierdzeniom dwie miary, które tworzą przedział mówiący o tym jak prawdopodobne coś jest, im mniejszy tym jesteśmy bardziej pewnii, w miarę pozyskiwania informacji przedział powinien się zawężać. 

## 3) Wnioskowanie niemonotoniczne

Modele wnioskowania oparte na logice klasycznej są **monotoniczne**, tzn. że jeśli rozszerzymy zbiór założen, to zbiór twierdzeń się nie zmniejsza.

Logikę która przy rozszerzaniu zbioru założeń możę zmniejszyć zbiór twierdzeń nazywamy logiką **niemonotoniczną**. Pozwala ona wnioskować o świece. (Przykład z autem, które zostało przejechane)

**Logika domniemań** - jest to logika, w której możemy twierdzić: *Jeżeli x jest ptakiem, to x lata, dopóki nie uzyskaliśmy informacji, że jest inaczej*.

**Regułą zamkniętego świata** - jeżeli czegoś nie ma w bazie wiedzy to nie istnieje.

**Logika autoepistemiczna** - zamiaast zbiorów twierdzeń są zbiory przekonań pozwala przykładowo wnioskować w ten sposób: *Jeżeli nie jestem przekonany, że jestem małżonkeim X, to nie jestem małżonkeim X, bo bym o tym na pewno wiedział*.

**Model rozumowań minimalnych** - ??

**Systemy zachowania spójności logicznej** - służą do tego aby po usunięciu jakiegoś założenia wszystkie i tylko twierdzenia z niego wynikające zostały usunięte w optymalny sposób. Najlprościej usunąć wszystkie konkluzje wyciągnięte z twierdzenia, jednak jest to ksoztowne. Ulepszona wersja mogłaby pamiętać o chronologi wprowadzania nowych informacji oraz wyprowadzania twierdzeń, wteyd możnaby łatwo usunąć te wynikające z niego. Można również pamię†ać dla każdego twierdzenia ciąg **uzasadnień**, wtedy system usuwa te twierdzenia, których istotnym elemnetm jest to twierdzenie, tak działają **systemy zachowania spójności logicznej oparte na uzasadnieniach.

**Systemy zachowania spójności logicznej oparte na założeniach** - w takich systemach znajdują się wszystkie uzasadnienia, które kiedykolwiek miały miejsce. Dla każego zdania w bazie danych system rejestruje **założenia**, które mogą być wyorzystane w jego wnioskowaniu
