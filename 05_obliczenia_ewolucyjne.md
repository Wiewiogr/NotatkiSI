# Obliczenia ewolucyjne

Grupa algorytmów inspirowanych biologią o największym znaczeniu. Polegają na symulacji natury w aspekcie procesów ewolucji.

## 1) Algorytmy genetyczne

**Przesztrzeń rozwiązań** przeszukujemy dla wielu punktów, w tym przypadku dla **osobników** tzn. każdy osobnik jest reprezentatem jakiegoś rozwiązania problemu. Zbiór osobnników w danym etapie obliczeń znajdjący się w przestrzeni roziwązań nazywamy **populacją**. Następujące po sobie populacje nazywamy kolejnymi pokoleniami. **Przestrzeń stanów** jest utworzona przez kolejne populacja.

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

**MUTACJE**
