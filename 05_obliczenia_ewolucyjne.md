# Obliczenia ewolucyjne

Grupa algorytmów inspirowanych biologią o największym znaczeniu. Polegają na symulacji natury w aspekcie procesów ewolucji.

## 1) Algorytmy genetyczne

**Przesztrzeń rozwiązań** przeszukujemy dla wielu punktów, w tym przypadku dla **osobników** tzn. każdy osobnik jest reprezentatem jakiegoś rozwiązania problemu. Zbiór osobnników w danym etapie obliczeń znajdjący się w przestrzeni roziwązań nazywamy **populacją**. Następujące po sobie populacje nazywamy kolejnymi **pokoleniami**. **Przestrzeń stanów** jest utworzona przez kolejne populacja.

Pozycja każdego osobnika w przestrzeni stanów jest określona przez współrzędne. Współrzędne określają **genotyp**. Każda współrzędna jest kodowana binarnie w postaci ciągu **genów** (gen to taki bit). Więc kilka genów określa jedną współrzędną osobnika. Zbiór współrzedncyh danego osobnika nazywamy **fenotypem**. Ocena się stopień przystosowania osobnika za pomocą **funkcji przystosowania**, czyli inaczej jkość rozwiązania.

Schemat algorytmu (str. 60 rys. 5.2):

0. **Inicjacja populacji początkowej osobników** poprzez losowy wybór ustalonej liczby osobników. Póżniej następuje ocena osobników za pomocą funkcji przystosowania.
1. **Selekcja osobników** o największych wartościach przystosowania. Zbiór wyselekcjonowanych osobników stanowi **populację rodzicielską**, a zbiór ich potomków stanowi **populację potomków**. Najprostsza metoda selekcji, to **metoda ruletki** (str. 61), aby uniknąć zerowych szans pojawienia się w kolejnej populacji stosujemy **metodę rankingową** (str. 61).
2. **Utworzenie populacji potomków poprzez zastosowanie operatorów genetycznych**, pierwszy z nich to **operator krzyżowania** tzn. losujemy pary osobników populacji, wybieramy **punkt krzyżownania** i krzyżujemy je w tym punkcie. Można również zastosować **krzyżowanie wielopunktowe**. Istnieje również **operator mutacji**, polega on na zmianie wartości losowego genu losowego osobnika populacji na przeciwny.
3. **Ocena populacji** oraz sprawdzanie warunku zakończenia, jeżeli jest on spełniony, to wybieramy najlepszego osobnika.

## 2) Strategie ewolucyjne

W strategiach ewolucyjnych osobnik jest reprezentowany przez parę wektorów jeden odpowiadający umiejscowienia osobnika w przestrzeni rozwiązań, a drugi to ciąg parametrów metody.

Schemat algorytmu (str. 65 rys. 5.5):

0. **Zainicjowanie i ocena początkowej populacji rodzicielskiej**
1. **Utworzenie populacji potomków** - najpierw wybieramy odpowiednią ilość osobników, które będą brać w prokreacji danego potomka. Wybór poprzez losowanie ze zwracaniem. W kolejnym kroku krzyżujemy aby otrzymać wstępną wersję potomka. W trzecim mutujrmy fragment parametrów metody a wczwartym za pomocą zmutowanego parametru przeprowadza się mutacje osobnika.
2. **Ocena populacji potomków**
3. **Selekca osobników do nowej populacji rodzicielskiej**, są dwie wersje, w jednej wybiera się najlepszych z populacji rodzicielskiej i potomków, a wdrugiej tylko z populacji potomków. 

Pod koniec cyklu sprawdzamy, czy spełniony jest warunek zakończenia, jeżęli tak, to wybieramy najlepszego osobnika jako rozwiązanie problemu.

*/\*doczytać o oznaczeniach \*/*

Najbardziej naturalnym sposobem zdefiniowania **operatora krzyżowania** jest obliczenie średniej z wartości genów należących do rodziców. Alternatywna wersja, to podmiana pojedyńczych genów osobników rodzicielskich.

**Mutacja** - na początku mutujemy parametry metody mnożąc je przez pewien czynnik wygenerowany za pomocą rozkłądu normalnego, po tym dodajemy go do wektora rozwiązań. (str. 67)

## 3) Programowanie ewolucyjne

W tej metodzie korzystamy z metafory gatunków. Mechanizmy tak zrobione aby aby preferowane były małe zmiany nad radykalnymi. Nie zakłada się również formy reprezenatcji osobników(w alg. genetycznych -binarna, a w strategiach ewolucyjnych wektorowa)

Schemat postępowania: (str. 68)

0. **Inicjowanie i ocena populacji R**.
1. **Utworzenie populacji potomnej P** poprzez losową mutację(zgodne z rozkładem normalnym) mutację każdego elemenu z populacji R.
2. **Ocena populacji P**.
3. **Utworzenie nowej populacji R** poprzez selekcję elementów z dotychczasowej populacji R i populacji P. (W klasycznej wersji metodą rankingową). 

Pod koniec cyklu sprawdzamy, czy spełniony jest warunek zakończenia, jeżęli tak, to wybieramy najlepszego osobnika jako rozwiązanie problemu.

Inna metoda selekcji, to *selekcja turniejowa*, w kórej dzielimy populację na grupy i w ramach każdej z nich dokonujemy selekcji.

## 4) Programowanie genetyczne

W programowaniu genetycznym tworzy się populacją programów i przeszukuje się przestrzeń możliwych programów w celu znalezienia najlepszego.

Aby coś takiego działało należy dostarczyć takiemu systemowi pewne elementy:
- musi znać elementarne komponenty z których może komponować programy.
- funkcję przystosowania(jak dobrze rozwiązuje postawione mu zadanie)
- możliwość sterowania tym generatorem rozwiązań np. wielkość populacji, kryterium zakończenia, prawdopodobieństwa stosowania operatorów genetycznych.

W programowaniu genetycznycm programy reprezentuje się najczęściej jako grafy lub drzewa. (przykład str. 71)

Podstawowoym operatorem jest krzyżowanie, a mutacja pełni drugorzędną rolę.

## 5) Inne modele inspirowane biologią

 **Inteligencja grupowa(stadna)** - polega na modelowaniu systemu jako samoorganizującej się populacji autonomicznych jednostek oddziałujących na siebie oraz na środowisko, w który się znajdują. Te jednostki moga mieć postać:
 - **agenta** - który transformuje obserwacje w akcje
 - **boidu**, które działają w stadzie według trzech reguł: rozdzielności, spójności i wyrównywania.
 
 W ramach tej grupy powstały np. **algorytmy mrówkowe** - opiera się na modelowaniu agentów jako mrówek, które szukają rozwiązań w przestrzeni rozwiązań pozostawiając ślad feromonowy. Dla obiecujących miejsc wartości feromonu sa wysoki, dla kiepskich - niskie.
 
 **Optymalizacja rojem cząstek** - metoda wyszukiwania najlepszego rozwiązania w n-wymiarowej przestrzeni rozwiązań. Rozwiązanie jest poszukiwane przez rój cząstek, przez analogię do stada ptaków podążającego za przywódcą, rój podąża za najlepszym rozwiązaniem.
 
 **Sztuczne systemy immunologiczne** - służy do rozwiązywania problemów, w których istotnym elementem jest wyszukiwanie anomali, przez analogię do układu immunologicznego, gdzie norma jest czymś pożądanym, a anomalie przypadkiem złym. W takim systemie, anomalie to wszystkie przypadki, które nie są znane. System poznając takie przypadki uczy się jakie anomalie mogą wystąpić. Są tutaj jeszcze detektory anomali, które po uruchomieniu się przez pojawienie się odpowiedniej anomali mutuje się i powiela.(doczytać str.73) 
