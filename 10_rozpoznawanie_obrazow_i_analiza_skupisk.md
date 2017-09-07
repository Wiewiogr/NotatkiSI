# Rozpoznawanie obrazów i analiza skupisk

## 1) Zadanie rozpoznawania obrazów

Każdy obraz jest reprezentowany prze **wektor cech**, warunkiem wykorzystania metod rozpoznawania jest dysponowanie przez nas tzw. ciągiem uczącym.

Etapy poprzedzające proces klasyfikacji:
- **przetwarzanie wstępne** - głównie redukcj zniekształceń pomiarowych(najczęściej metodami filtracji sygnałów) oraz normalizacja obrazu(do odpowiednich wartości z przediałów),
- **ekstrakcja cech** - redukcja liczby cech wektorów, wybieramy do klasywikacji tylko te cechy które są nam potrzebne, tak aby najmniejszą możliwą liczbę cech,
- **selekcja cech** - należy wybrać podzbiór cech posiadających odpowiednią moc dyskryminacyjną tzn. takich na podstawie których uzyskamy najmniejszy błąd klasyfikacji.

**Przestrzenią cech** nazywamy obiekty, czyli wektory cech wybrane w trakcie etapów powyżej. Obiekty, które w przestrzeni cech znajdują sie blisko siebie tworzą **skupisko**.

## 2) Klasyfikator minimalnoodległościowy

Aby zaklasyfikować obiekt do któregoś skupiska tą metodą musimy na początku wyznaczyć **wzorcowe obiekty** należące do każej z klas(skupisk), później liczymy odległość naszego obiektu do nich. Nasz obiekt należy do klasy dla której obliczona odległość była najmniejsza

## 3) Metoda najbliżeszego sąsiada

W tej metodzie wybieramy odległość nieznanego obrazu od wszystkich innych elementów ciągu uczącego, a następnie wybieramy klasę elementu, który był najbliżej naszego. Czasami stosuje się również **metodę k-najbliższych sąsiadów k-NN** (gdzie k to mała liczba nieparzysta), w tej metodzie szuka się k najblizszych sąsiadów i wybiera się klasę do której należy większość z nich.

## 4) Klasyfikatory oparte na granicach decyzyjnych

**Klasyfikatory oparte na granicach decyzyjnych** próbują wyznaczyć granice klas w przestrzeni cech.

W najprostszym przypadku klasy mogą być oddzielone **liniową funkcją dyskryminacyjną**, tzn. oddzielamy od siebie skupiska liniami (str. 149 rys. 10.2)**Klasyfikator wektorów wspierających** służy do wyznaczania granicy pomiedzy dwoma skupiskami tak aby była jak największa. Wyznacza się dwie płaszczyzny równoległe do siebie i w środku pomiędzy nimi wyznacza się granice (str. 149 rys. 10.2d)

**Klasyfikatory nieliniowe** korzystają one z granic, które są funkcji wyższych stopni. Jednak trudno jest uzyskać efektywne algorytmy wyznaczające takie granice.

## 5) Metody statystyczne

Możemy dysponowć różnymi informacjami *a priori* np. obiektów A jest 4 razy więcej niż B. Powinniśmy znać gęstość rozkładu prawdopodobieństwa dla klas, tzn. prawdopodobieństwa warunkowe np. *prawdopodobieństwo, że obiekt mający 8 cm długości jest szprotką wynosi 0.75*.  

**Wzór Bayesa**
(nie mam pojęcia co się dzieje str. 151 - 153)

W meteodach statystycznych za pomocą wzoru Bayesa wyznacza się jakie jest prawdopodobieństwo, że posiadając jakieś cechy należy do danej klasy.

**Klasyfikator Bayesa** przypisuje obrazowi **o jednej cesze** klasę dla której prawdopodobieństwo jest największe.

**Naiwny klasyfikator Bayesa** dla obrazów o wielu cachach, traktuje każdą cechę niezależnie, jego wynik to iloczyn klasyfikatorów Bayesa dla wyszystkich.

## 6) Klasyfikator oparty na drzewach decyzyjnych

Powyższe metody należały do **jednoetapowego rozpoznawania obrazów** ponieważ przy klasyfikacji brało się pod uwagę naraz wszystkie cech obrazu. Innym rodzajem klasyfikacji jest **sekwencyjne rozpoznawanie obrazów**, którego jedną z najbardziej znanych technik jest **klasyfikator oparty na drzewach decyzyjnych**.

Metoda polega na podziale przestrzeni cech granicami równoległymi do osi układu współrzędnych. Granice te są konstruowane przez sekwencyjne ustalanie progów dla poszczególnych. Te podzialy można przedstwić jako drzewa. (str. 154 rys. 10.4)

## 7) Analiza skupisk

Metody analizy skupisk dzielimy na:
- **metody oparte na podziale**, w którym zakładamy, że przynajmniej wiemy na ile skupisk należy podzielić przykładowe obiekty,
- **metody hierarchiczne**, które wykorzystujemy, kiedy informacji o liczbie skupisk nie posiadamy

**Metoda k-średnich** to technika oparta na podziale, metoda ta wykorzystuje pojęcie **centroidu skupiska**, który jest średnią położenia wszystkich obrazów należących do skupiska. (opis metody str. 155-156)

W metodach hierarchicznych istnieją **metody aglomeracyjne** (mogące połączyć w większe skupiska) oraz **metody rozdzielające** dekomponujące na mniejsze skupiska. Schemat działania:
1. Wyznacz pojedyńcze skupiska, gdzie każde składa się z jednego obiektu oraz policz odległości między nimi
2. Znajdz pare najblizszych skupisk i połącz je w jedno nowe skupisko
3. Oblicz odległości między nowym skupiskiem a pozostałymi
4. Powtarzaj kroki 2 oraz 3, aż powstanie jedno wielkie skupisko.

Metody obliczania odległośći między skupiskami:
- **metoda pojedynczego wiazania** - odległość między skupiskami to odległość między dwoma najbliższymi obiektami
- **metoda całkowitego wiązania** - odległość między skupiskami to odległość między dwoma najdalszymi obiektami
- **metoda centroidów** - obliczamy odległość mięzy centroidami skupisk
