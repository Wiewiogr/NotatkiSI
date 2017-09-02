# Syntaktyczna analiza wzorców

W tej metodzie wnioskowania dokonoju się na podstawie struktur opisujących świat zewnętrzny. Zbiór struktur/wzorców odpowiada bazie wiedzy. Zbiór taki nie jest zapisany w bazie wiedzy bezpośrednio, ale za pomocą systemu generującego wszystkie wzorce tego zbioru, tzw gramatyki generatywnej.

## 1) Generowanie reprezentacji strukturalnych

Aby skonstruować **gramatykę generatywną** potrzebny jest **zbiór symboli(etykiet) terminalnych**, z którego będziemy budować zdania należące do tego języka. Po prostu słowa, z których powstaną zdania.

**Produkcje** - są to reguły przepisujące (przykład na str.108 8.1, 8.2), są w nich **symbole pomocnicze (nieterminalne)**. Produkcje składają się z **lewej strony produkcji** oraz **prawej strony produkcji**. Zastosowanie produkcji polega na podmianie w frazy tożsamej z lewą stroną produkcji na prawą stronę. Sekwencja zastosowanych produkcji dążąca do wygenerowania danego zdania nazywana jest **wywodem/wyprowadzeniem** tego zdania, które składa się z **kroków wywodu**.

Istnieje również **zbiór symboli terminalych**. Gdy definiujemy gramatykę wyróżniony jest symbol nieterminalny od którego zaczynamy generowanie zdań, nazywa się on **symbolem startowym (etykietą startową lub aksjomatem)** i jest oznazany literką S. Istnieje również **słowo puste**.

Istnieje wiele rozdajów klas gramatyk generatywnych, można je ułożyć w hierarchię według kryterium **mocy generacyjnej (opisowej)**. Rodzaje gramatyk ze względu na moc obliczeniową:
- **gramatyka regularna** - pozwala jedynie doklejać symbol na końcu wyprowadzonego wyrażenia ( najsłabsza generacyjnie gramatyka)
- **gramatyka bezkontekstowa** - nie wprowadzają żadnych ograniczeń poza tym, że po lewej stronie musi się znajdować pojedyńczy symbol terminalny.

## 2) Analiza reprezentacji strukturalnych

**Automaty formalne** służą do analizy gramatyk generatywnych, mogą się one różnić konstrukcją w zależności od języka dla którego zostały stworzone. 

Automaty można przedstawiać jako grafy, wierzchołki prezentują **stany**, wyróżniamy **stan początkowy** oraz **stan końcowy**, skierowane krawędzie grafu oznaczają **prześcia/tranzycje**. **Funkcje przejścia** to funkcje, któ®ych argumentem jest para, wyznaczają one miejsce do którego automat powinien się przenieść.

**Automat skończony** to najprostszy typ automatów, stworzony do analizy *języków reguralnych* generowanych przez *gramatyki regularne*. (str. 113 rys. 8.1) Istnieją metody jego generowania na podstawie odpowiadającej mu gramatyki. Wynikami funkcji przejścia mogą być:
- *akceptuj*
- *odrzuć*

Aby analizować **język bezkontekstowy** potrzebny jest automat o odpowiednej mocy tzw. **automat ze stosem**. Jego funkcja przejścia zbudowana jest w nieco inny sposób tzn. jej wynikami mogą być:
- *akceptuj*
- *odrzuć*
- *usun_symbol*
- *zastosuj_produkcje_na_stosie*

Im większa moc obliczeniowa automatów, tym większa złożoność obliczeniowa analizy. Dlatego powstały specjalne podklasy gramatyk bezkontekstowych, dla których można generować bardziej efektywn automaty np.
- LL(k)
- LR(k)
- precedensyjne

Silniejsze klasy gramatyk to:
- **gramatyka kontekstowa**, a jego analiator **automat liniowo ograniczony**,
- **gramatyka typu 0** - **maszyna turinga**

## 3) Interpretacja reprezentacji strukturalnych

Omówione powyżej automaty to tzw. **akceptory** ponieważ ich zadaniem było sprawdzanie, czy dane wyrażenie należy do języka.

Inną grupą automatów są **transdjusery (automaty z wyjściem)**, które w trakcie analizy jakiegoś wyrażenia generują na wyjście inne wyrażenie np. tłumaczenie. *Funkcje przejścia* w takich automatach nie tylko wyznaczają nowy stan, ale wypisują również na wyjście symbole. Takie coś ma zastosowanie w NLP.

Możemy korzystać z automatów nie tylko w NLP, ale również do reprezentacji graficznych np. wykresów. Elementy reprezentowane przez *symbole terminalne* np. strzałki, proste, łuki nazywamy **składowymi pierwotnymi**. Np. wykresy EKG.

**Gramatyki atrybuowane** to takie gramatyki, w których składowe poza symbolem posiadają również jakieś dodatkowe atrybuty (np. kąt nachylenia, długość).

**Gramatyki stochsatyczny/probablistyczne**, które dla każego symbolu dopisują dodatkowo wzorcowe wartości i odchylenia. **Automat stochastyczny** analizując takie wyrażenia generuje na wyjście prawdopodobieństwo użycia danej produkcji. 

Istenieją metryki, które pozwalają mierzyć odległość mięzy wzorcem a strukturalnie zniekształconym obrazem np. **metryki Levenshteina**.

Zastosowania:
- EKG, EEG, PWA, ABR (jakieś badania)
- analiza zjawisk ekonomicznych

## 4) Indukcja gramatyki generatywnej

**Induckji (wnioskowania) gramatyk generatywnych** polega na wykorzystaniu **pochodnej symbolicznej**.

(opis obliczania pochodnych na str. 122)

Jeżeli mamy zbiór jakiś wyrażeń możemy obliczyć jego wszystkie pochodne symboliczne i w ten sposób otrzymać produkcje jakie zostały użyte to utworzenia tych wyrażeń.

## 5) Wielowymiarowe gramatyki generatywne

**Systemy przepisujące grafy** służa do przekształcania struktur o charakterze grafów, najbardziej powszechnie używanym ich przykładem są **gramatyki grafowe**.

(przykładzik str.124)

Podstawowy problem w gramatykach grafowych jest zastępowanie grafu lewej strony produkcji przez graf prawej strony, odpowiedzialna za tę sytuację jest **transformacja osadzenia**

**Gramatyki edNLC** opisane na str. 125-126

Jedynie dla podklasy **gramatyk grafowych ETPL(k)** udało się skonstruować efektywne automaty garfowe. Mają zastosowanie m.in. w systemach ekspertowych, analizie obrazów, w systemach wieloagentowych.

