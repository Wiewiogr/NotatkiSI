# Symboliczna sztuczna inteligencja

wspólne założenia podejść tego nurtu:
- możliwe jest skonstruowanie modelu reprezentującego system inteligentny explicite
- wiedza w tych modelach powinna być reprezentowana w sposób symboliczny(np. w postaci grafów, wyrażeń loginczych itd.)
- (inteligentne) działania umysłowo-poznawcze można opisać przy użyciu formalnych operacji nad wyrażeniami i strukturami symbolicznymi należącymi do modelu wiedzy.

## 1) Symulacja kognitywna

Postawą tego podejścia jest konstrukcja algorytmów heurystycznych (dostarcza akceptowalne rozwiązanie, dla którego nie możemy przeprowadzić dowodu jego poprawności) w celu symulacji ludzkich procesów umysłowo poznawczych.
Na podstawie tego podejścia powstał *Logic Theorist* oraz *General Problem Solver*.
Cztery podstawowe elementy modelu symulacji kognitywnej:
- **przestrzeń stanów** - jest to graf, w którym wierzchołki odpowiadają stanom, a krawędzie dopuszczalnym przejściom
- **rozwiązywania problemów przez heurystyczne przeszukiwanie** - polega na tym, że nie mając algorytmu rozwiązującego problem możemy wciąż go rozwiązywać metodą prób i błędów, nie koniecznie na ślepo, możemy korzystać z jakiejś wiedzy. Dodatkowo taka metoda powinna generować każde rozwiązanie tylko raz, oraz być w stanie wygenerować wszystkie.
- **analiza celów i środków** - polega na tym, że sprawdzamy różnicę pomiędzy stanem aktualnym a stanem docelowym i tak samo dla potencjalnych kolejnych stanów i wybieramy taki następny stan, w którym ta różnica będzie jak najmniejsza.
- **redukcja problemu** - polega na rozbijaniu problemów na mniejsze prostsze podproblemy, ponieważ dla każdego takiego podproblemu może być inna przestrzeń stanów, albo może być użyta inna metoda *analizy celów i środków*.

## 2) Podejście oparte na logice

**Paradygmat deklaratywny** - podajemy jedynie jakie wartości powinny się zawierać w rozwiązaniu problemu, a oprogramowanie na komputerze(interpreter, kompilator itd.) sam dobiera odpowiednie funkcje. Inaczej niż w *paradygmacie imperatywnym*, w którym kod jest sekwencją operacji do wykonania.
W ramach tego paradygmatu wyróżniamy dwa podejścia:
- **programowanie logiczne** - zapisujemy nasze oczekiwane rozwiązanie w postaci twierdzeń logicznych, a system SI za pomocą wnioskowania logicznego i twierdzeń logicznych, które posiada wyznacza rozwiązanie.
- **programowanie funkcyjne** - oparte na *rachunku lambda*, specyfikacja pożądanych własności rozwiązania zapisana jest jako złożona funkcja. W systemie informatycznym funkcje takie są reprezentowane przez wyrażenia odpowiadające wyrażeniom rachunku lambda. Oprogramowanie na komputerze musi być w stanie interpretować takie wyrażenia.

## 3) Regułowa reprezentacja wiedzy

**System oparty na produkcjach** - podstawowe komponenty tego modelu to:
- **pamięc reguł** odpowiada pamięci długotrwałej, zapisywane są tam reguły postaci *Jeśli X, to wykonaj akcję Y*. Jako, że odpowiada to pamięci długotrwałej zakładmy, że reguły zostaną tam na stałe.
- **pamięć robocza** odpowiada pamięci krótkotrwałej, jest to pamięć dynamiczna. Informacje w niej zawarte są sprawdzanie w ciągłym cyklu.

## 4) Strukturalna reprezentacja wiedzdy

Podział wiedzy na:
- **wiedzę deklaratywną** - wiedzę o faktach, wiedzę *"że"*
- **wiedzę proceduralną** - wiedzę o postępowaniu, wiedzę *"jak"*

*/\*doczytać drugi paragraf\*/*

modele:
- **sieci semantyczne** - wierzchołki reprezentują obiekty lub pojęcia, a krawędzie relacje(*jest-typu* lub *jest-podklasą*).
- **ramy** - rozbudowane sieci semantycznew taki sposób, że wierzchołki mają bardzo bogatą strukturę określającą dokładnie obiekty i pojęcia.
- **sktypty** - jest reprezentacją stereotypowej akcji np. za pomocą grafów zależności pojęciowej

## 5) Podejście oparte na lingwistyce matematycznej

**Gramatyka generatywna** - służy jako generator dowolnego zdania nieskończonego języka. W celu analizy zdań danego języka możemy stworzyć dla jego gramatyki **automat formalny**. 
