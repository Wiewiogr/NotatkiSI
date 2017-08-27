# Przeszukiwanie przestrzeni stanów

Podstawową ideą tego podejścia jest konstrukcja algorytmów symulująca ludzkie procesy umysłowo poznawcze.

## 1) Przestrzeń stanów i drzewo przeszukiwań

1. Na początku tworzymy **abstrakcyjny model opisu problemu** (abstrakcyjny bo uwzględniamy jedynie interesujące nas aspekty. (przykład na s.36 - od 4.1a przechodzimy do 4.1c)

2. Konstruujemy **przestrzeń stanów**, jest to graf, którego wierzchołki są możliwymi **stanami**, a krawędzie przejściami z jednego stanu do drugiego. Wyróżniamy:
- **wierzchołek początkowy**
- **wierzchołek końcowy**

Przy takiej reprezentacji rozwiązanie problemu sprowadza się do znalezienia drogi od wierzchołka początkowego do końcowego.

Jako, że przestrzeń stanów jest zwykla bardzo duża, dlatego generujemy i analizujemy krok po kroku tylko te stany, które bierzemy pod uwagę w kolejnych krokach, tworząc przy tym **drzewo przeszukiwań**. (przykład s. 38 )

*Strategie przeszukiwania* przestrzeni stanów możemy podzielić na:
- **metody przeszukiwania ślepego**
- **metody przeszukiwani aheurystycznego**

## 2) Przeszukiwanie ślepe

(str. 40 rys. 4.3 - opisane drzewo)

**rząd wierzchołka** to ilość jego bezpośrednich potomków.

- **przeszukiwanie wszerz** - generowanie kolejnych wierzchołków poziom po poziomie. (str. 40 rys 4.3) Drzewo jest generowane do momentu znalezienia stanu końcowego. Dobre rezultaty, jeśli rzędy wierzchołków nie są duże, tzn. jeśli drzewo nie jest "szerokie" i "płytkie"

- **przeszukiwanie w głąb** - generowanie dla wierzchołka poziomu n jedynie jednego wierzchołka poziomu n+1 i dalej tylko jednego n+2 itd. jeśli dotarliśmy do liścia, który nie jest rozwiązaniem cofamy się o jeden poziom i próbujemy iść w głąb, jeżeli nie możemy, to dalej się cofamy itd. (str. 42 rys. 4.4) Dobrze działa dla drzew "szerokich" i "płytkich". Kiepsko działa, gdy niektóre wierzchołki są bardzo głębokie inne płytkie, dlatego powstały metody poniżej.

- **ograniczone przeszukiwanie w głąb** - generujemy wierzchołki jak w metodzie *w głąb* ale tylko do pewnego poziomu, jeśli doszliśmy do tego poziomu, to traktujemy go jak liść, który nie jest rozwiązaniem i wycofujemy się. Metoda ta zadziałą, jeżeli jesteśmy w stanie dobrze wyznaczyć poziom do którego chcemy się zagłębiać, inaczej można pominąć rozwiązanie, dlatego powastała metoda poniżej.

- **przeszukiwania pogłębianego iteracyjnie** - działa jak metoda powyżej dla poziomu l, jednak jeżeli nie uda się znaleźć rozwiązania dla tego poziomu, to szukamy dla l+1, potem dla l+2 itd. aż znajdziemy rozwiązanie.

- **przeszukiwanie o jednolitym koszcie** - oparta na schemacie szukania najkrótszych ścieżek Dijkistry. Modyfikacja przeszukiwania wszerz, zamiast generować wierzchołki w losowej kolejności najpierw generujemy te do których koszt przejścia jest najmniejszy.

## 3) Przeszukiwanie heurystyczne

**funkcja heurystyczna** - szacuje jak blisko rozwiązania jest dany wierzchołek. Te metody polegają na rozwijaniu tych ścieżek *drzewa przeszukiwań*, które wydają się być najbliżej rozwiązania.

- metoda **przeszukiwania wspinaczkowego** - jest to modyfikacja przeszukiwania w głąb, w której rozwijamy te wierzchołki drzewa, dla których funkcja heurystyczna zwraca największą wartość. Jest to metoda *przeszukiwania lokalnego*, ponieważ w każdym kroku możemy się przenieść do stanu sąsiedniego.

- **przeszukiwanie pierwszy-najlepszy** - jeżeli przeszukując tak jak w metodzie powyżej natkniemy się na wierzchołek gorszy niż poprzedni, szukamy w wygenerowanym już drzewie najbarzdiej obiecującego wierzchołka i tam się przenosimy.

- **przeszukiwanie A** - wyboru kolejnego wierzchołka ddokonuje się na podstawie wartości funkcji heurystycznej oraz kosztu przejścia do niego. Oba te kryteria są składowymi **funkcji oceny** f:
> f(n) = g(n) + h(n)
g(n) - funkcja kosztu dotarcia do wierzchołka n od korzenia, h(n) - funkcja kosztu dotarcia od wierzchołka n do celu (heurystyczna)

- **przeszukiwanie wiązką** - rozwijamy w przeszukiwaniu w wszerz drzewo poziom po poziomie, jednak na każdym poziomie zostawiamy do dalszego rozwinięcia tylko *b* najlepszych

Właściwości funkcji heurystycznej:
- **dopuszczalność** - szacując odległość od wierzchołka do celu funkcja nigdy nie przekracza tej wartości, ale może być trochę mniejsza.
- **spójna** - im bliżej celu tym bardziej dokładne wartości zwracane przez funkcję.
- **dominacja** - jeżeli mamy dwie funkcje spełniające powyższe własności, ale h1(v) >= h2(v), to funkcja h1 *dominuje* funkcję h2. W przypadku funkcji heurystycznych lepiej jest używać funkcji dominujących.

## 4) Przeszukiwanie z przeciwnikiem

