# Strukturalne modele reprezentacji wiedzy

**Ontologia** - formalna specyfikacja pojęć(konceptualizacja) pewnej dziedziny skonstruowana tak, aby można ją było wykorzystywać do rozwiązywania różnych problemów( w zakresie tej dziedziny) za pomocą standardowych procedur wnioskowania.

## 1) Sieci semantyczne

To takie sieci, które mogą pokazywać np. dziedziczenie, są zależności jak *jest podklasą*, a w logikach deskrypcyjnych takie coś byłoby nazywane *ogólną inkluzją pojęć*. (str. 97 rys. 7.1)

Elementarne, podstawowe **pojęcia(klasy)** służące do definiowania innych nazywamy **pojęciami atomowymi**. (przykład z kolorami na str. 98 akapit 2). Takie pojęcia(klasy) możemy instancjonować tworząc **obiekty** lub **instancje**. Klasy możemy traktować jako zbiory obiektów, można obiekty mogą posiadać etykietę, że *należą do klasy*. Kolejnym elementem sieci semantycznych są **role**, które odzwierciedlają relacje zachodzące pomiędzy obiektami i klasami, podobnie jak w przypadku pojęć istnieją **role atomowe**, dzięki którym myożna definiować bardziej złożone pojęcia. (str. 99 rys. 7.2)

Najprostszą metodą ekstrakcji wiedzy z sieci semantycznych jest **metoda dopasowywania strukturalnego**, aby zweryfikować prawdziwość jakiegoś twierdzenia definiujemy ogólny wzorzec i staramy się go dopasować do naszej sieci.

Podstawowym problem we wnioskowaniu w sieciach semantycznych jest złożoność obliczeniowa, jako, że sieci semantyczne to grafy, to jest to złożoność niewielomianowa.

## 2) Ramy

**Ramy** można traktować jako rozszerzenie sieci semantycznych. Każdy wierzchołek w ramach posiada swoją wewnętrzną strukturę, która pozwala go dokładniej scharakterysować. ( mówimy wtedy o *ramie obiektu* albo o *ramie klasy*).

Rama składa się z **klatek**, które reprezentują własności obiektu lub pojęcia. Każda cecha może być charakteryzowana w wielu **aspektach**.

Podstawowym mechanizmem wnioskowani jest **dziedziczenie**, tzn. wiedza z klasy po której dany obiekt dziedziczy może być propagowana do niego. Możliwe jest również **dziedziczenie wielokrotne**.

Drugim mechanizmem wnioskowania są tzw. **procedury demoniczne**, inaczej zwane **demonami**. Jest to niestatyczna wersja *aspektu* klatki ramy. Najczęściej aktywizuje się w reakcji na jakieś zdarzenie. (przykład na 102 - 103)

Ramy wywarły ogromny wpływ na programowanie obiektowe.

Podstawowym problemem systemów SI opartych na ramach jest szybkość.

## 3) Skrypty

Metoda stosowana w przetwarzaniu języka naturalnego.

Model ten mówi, że jeśli chcemy zrozumieć przekaz językowy dotyczący pewnego wydarzenia(historyjka, relacja), to odwołujemy się do pewnego uogólnionego wzorca(znajdującego się w naszej pamięci). Taki uogólniony wzorzec jest konstruowany w naszej pamięci na podstawie doświadczeń w trakcie powtarzających sie wielokrotnie wydarzeń. Wydarzenia składają się z sekwencji **zdarzeń elementarnych**.

**Skrypt** można zdefiniować jako strukturalną reprezentację opisującą jakieś wydarzenie za pomocą stereotypowej sekwencj zdarzeń elementarnych. Sformalizowany skrypt posiada:
- agentów
- rekwizyty
- akcje
- warunki począ†kowe
- rezultaty

Taka reprezentacja wiedzy mówi o tym, jaki(typowy) przebieg mają pewne wydarzenia. Wiedza taka może służyć do przewidywania kolejnych zdarzeń elementarnych danego wydarzenia lub do wnioskowania typu: "co zrobć aby osiągnąć dany cel?". W przypadku NLP jeżeli w przekazie słownym brakuje jakiejś informacji jesteśmy w stanie domyśleć się na podstawie uogólnionego wzorca.

(przykład na str. 106)
