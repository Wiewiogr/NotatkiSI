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
