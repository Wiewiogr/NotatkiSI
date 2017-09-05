# Wnioskowanie oparte na logice

Podejście do wnioskowania jak do dowodzenia twierdzeń.

## 1) Opis świata za pomocą logii pierwszego rzędu

W logice pierwszego rzędu będziemy opisywać świat głównie elementami zwanymi **termami** do których należą:
- **Symbole tzw. stałych indywiduowych** - odpowiadają one konkretnym obiektom (instancjom jakiś klas)
- **Symbole tzw. zmiennych indywiduowych** - przybierają wartości różnych obiektów
- **SYmbole funkcji** - przypisują jednym obiektom inne

Dodatkowo do języka opisu należą **symbole predykatów**, które możemy traktować jako funkcje działające na termach, kóre zwracają prawdę bądź fałsz. Predykat z zapisanymi argumentami to **formuła atomowa**. Potrzebne są również **operatory logiczne** oraz **kwantyfikatory** za których pomocą można z *formuł atomowych* tworzyć **formuły**. Kwantyfikatory wiążą zmienne, zmienna może być **związana** lub może być **zmienną wolną**.

Zbiór przedmiotów indywiuowych to **uniwersum**. **Interpretacja** jest przyporządkowaniem **znaczenia** elementom języka logiki. **Struktura** to relacje zachodzące??

**Formuła prawdziwa(tautologia)** to formuła która jest spełniona w każdej strukturze przy dowolnym wartościowaniu.

W systemach SI konstruuje się system wnioskowania, który weryfikuje nieznaną formułę przez wnioskowanie na podstawie formuł uznanych za prawdziwe, w systemie takim znajdują się przynajmniej:
- **Aksjomaty** - to formuły, których prawdziwość zakłądamy, stranowią podstawową bazę wiedzy systemu.
- **Reguły wnioskowania (inferencyjne)** - są wzorcami służącymi do wyprowadznia nowych formuł ze znanych formuł. (to są te reguły z kolosa)

Konstruuje się systemy wnioskowania, który weryfikuje nieznaną formułę przez wnioskowanie na podstawie formuł uznanych za prawdziwe.

Podsumowując wrzucamy do systemu formułę On patrzy w systemie na podstawie innych, czy jest prawdziwa, wykorzystuje do tego reguły inferencyjne i zwraca wynik.

## 2) Wnioskowanie za pomocą metody rezolucji

**Metoda rezolucji** opiera się na sposobie dowodzenia twierdzeń nie wprost, czyli tworzymy zaprzeczenie tezy której chcemy dowieść i wskazujemy sprzeczność między tym zaprzeczeinem a przyjętymmi założeniami.

**Rezolwenta** to formuła wynikowa każdego kroku, formuły wejściowe to **formuły kolidujące**. 

(To też będzie na kolosie)

## 3) Sposoby sprowadzania formuł do postaci normalnych

(To też na kolosie)

## 4) Szczególne postaci formuł w systemach wnioskowania

**Prolog** można uznać za "klasyczny" język programowania służący do budowania systemów wnioskowania oparty na metodzie rezolucji.

Na kolosie też **postać klauzulowa**.

## 5) Wnioskowanie jako obliczanie symboliczne

We wnioskowaniu przez obliczanie symboliczne przekształcenia odbywają bez wnikania w znaczenie symboli i wyrażeń, opiera się na **regułach przepisujących termy**.

Obliczenia są skończone, gdy doprowadzimy wyrażenie do **postaci normalnej** tzn. takiej, w której nie możńa zastosować już żadnej reguły.

W obliczeniach kolejność wykonywania działań nie ma znaczenia tzn. te obliczenia mają **własność Churcha-Rossera**. 

**Rachunek lambda** to jeden z najbardziej popularnych systemów przepisujących termy. Był on próbą konstrukcji formalnego systemu, w którym dowodzenia twierdzeń miałoby charakter symbolicznego obliczania, w którym nie wnikamy w semantykę przekształcanych wyrażeń.

(Zasady rachunku lamnbda na stronach 89-94)

W rachunku lambda możemy przedstawić wszystkie konstrukcje programistyczne wykorzystywane w informatyce.

**Lisp** był inspitorwany rachunkiem lambda.


