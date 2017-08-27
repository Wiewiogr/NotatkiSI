# Inteligencja obliczeniowa

wspólne cechy modeli tego podejścia:
- w reprezentacji wiedzy podstawową rolę odgrywa informacja numeryczna (liczbowa)
- przetwarzanie wiedzy oparte jest głównie na obliczeniach na liczbach
- zazwyczaj wiedza nie jest reprezentowana explicite

do inteligencji obliczeniowej należą:
- sieci neuronowe,
- rozpoznawanie obrazów,
- analiza skupisk,
- wynioskowanie probabilistyczne,
- modele oparte na zbiorach rozmytych,
- modele oparte na zbiorach przybliżonych,
- obliczenia ewolucyjne,
- modele inteligencji stadnej,
- optymalizacja rojem cząstek,
- sztuczne systemy immunologiczne

## 1) modele konekcjonistyczne

**podejście asocjacyjne** według niego podstawowym mechanizmem procesów umysłowych jest kojarzenie, później zostało rozwinięte w **podejście konekcjonistyczne**. Zgodnie z tym uczenie jest wynikiem asocjacji, które powstają między bodźcem i odpowiedzią na ten bodziec.

w tych modelach asocjacje są reprezentowane za pomocą **sieci konekcjonistycznych**, które dzielimy na dwie kategorie:
- **sieci konekcjonistyczne z reprezentacją lokalną** - sieć, w której każdy składnik wiedzy jest zapamiętany przez pojedyńczy element sieci. (np. sieci semanntyczne)
- **sieci konekcjonistyczne z reprezentacją rozproszoną** - zapamiętana wiedza jest rozdystrybuowana między wiele elementów sieci. (np. sieci neuronowe)

## 2) modele inspirowane matematyką

**rozpoznawanie obrazów** - polega na rozpoznawaniu obiektów. Są one reprezentowane za pomocą zespołów cech. Rozpoznawania nieznanych obiektów dokonuje się za pomocą *klasyfikatora*, który wyznacza do jakiej grupy dane obiekty należą, aby skonstruwać taki klasyfikator potrzebujemy obiektów należących do tej kategorii.
**analiza skupisk** - wykrywanie kategorii, na jakie można podzielić.

modele oparte na **sieciach bayesowskich** służą do wnioskowania na podstawie stwierdzeń z dodanym do nich prawdopodobieństwem, która nie tyle ocenia stopień prawdziwości, ale bardziej stopień niepewności.

modele oparte na **teorii Dempstera-Shafera** uwzględniają czynnik brakku wiedzy w procesie wnioskowania.

**logika niemonotoniczna** może zostać użyta, gdy stwierdzenia mogą przestać być prawdziwymi w odróżnieniu od logiki klasycznej.

## 3) modele inspitowane biologią

**obliczenia ewolucyjne** - cechą wspólną tych metod jest generowanie i analiza wielu rozwiązań w danym kroku. Każde takie rozwiązanie jest traktowane jako osobnik populacji. Osobniki poddawane są mutacjom, krzyżowaniu. Największą szanse na przejście do kolejnego pokolenia mają osobniki, które zostały najlepiej ocenione za pomocą *funkcji przystosowania*. Za pomocą sekwencji tych kroków generujemy kolejne pokolenia aż algorytm osiągnie warunek zakończenia.

algorytmy ewolucyjne dzielą się na:
- **algorytmy genetyczne**
- **strategie ewolucyjne**
- **programowanie ewolucyjne**
- **programowanie genetyczne**

Generalnie metody róznią się od siebie:
- sposobem reprezentacji osobników,
- rolą odgrywaną przez operatory (mutacja, krzyżowanie)
- sposobem tworzenia nowej populacji


