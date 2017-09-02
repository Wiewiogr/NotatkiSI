# Systemy regułowe

Są to modele polegające na wnioskowaniu dedukcyjny, z tym że wiedza jest reprezentowana za pomocą czytelnych reguł postaci: " jeżeli coś to coś".

## 1) Model systemu regułowego

(str. 129 rys. 9.1)

**Pamięć robocza** zawiera reprezentacje **faktów** o zewnętrznym świecie o ktorym system będzie przeprowadzal wnioskowania. Może zawierać również inne informacje niezbędne w procesie wnioskowania np. **hipotezy robocze** lub **struktury (sieci) podstawień**(powiązania między zmiennymi, gdy dokonujemy podstawienia).

Wnioskowanie w systemie ma postać **reguł**: 

> IF *COND* THEN *ACT*

COND - **warunek (poprzedznik) reguły** , a ACT - **akcja (następnik) reguły**. Warunek ma postać koniunkcji **warunków elementarnych** (prostych predyktaów).

Spełnienie warunku znaczy, że w bazie wiedzy znajdują się fakty, które po wstawieniu do warunku powodują przyjęcie przez niego wartości *Prawda*.

Akcja *ACT* w przypadku **reguł typu deklaratywnego** charakter wniosku wynikającego z warunku reguły. Wyciągnięcie wniosku oznacza zmodyfikowanie pamięci roboczej np. modyfikacja zmiennej albo dodanie jakiegoś faktu.W przypadku **reguł typu reaktywnego** akcja może zawierać też wywołanie jakiejś zemnętrznej operacji.

Reguły są gromadzone w **bazie reguł**.

Wnioskowaniem steruje **moduł wnioskowania (interpreter reguł, maszyna wnioskująca)**, cykl pracy składa się z trzech etapów:
- **dopasowanie reguł** moduł szuka reguł pasujących do faktów z pamięci roboczej tworząc **zbiór reguł konfliktowych**
- **rozstrzyganie konfliktu reguł** 

## 2) Strategie wnioskowani w systemach regułowych

Wnioskowanie w systemach regułowych jest **wnioskowaniem dedukcyjnym** i może przebiegać zgodnie z jedną z dwóch strategii:
- **wnioskowanie w przód** - moduł wnioskowania próbuje dopasować **warunek** którejś reguły do jakiegoś faktu znajdującego się w pamięci roboczej. Jeżeli pojawi się fakt pasujący do reguły, to reguła zostanie zastosowana, tzn. skutek wykonania **akcji** jest zostanie zapisany do pamięci roboczej, w innym przypadku nic się nie dzieje. Może się okazać, że po zostosowaniu akcji jakiś kolejny warunek zostaje spełniony, wtedy cykl wnioskowania się ponawia. (str. 131 rys 9.2) Dodatkowo moduł wnioskujący wie, że jakiś fakt wynikł z innego, dlatego drugi raz nie jest przeprowadzane dla niego wnioskowanie, m.in. to znajduje się poza faktami w pamięci roboczej.
- **wnioskowanie wstecz** - polega na zadawaniu systemowi pytań, czy dana reguła zachodzi w formie hipotez, której prawdziwości bądź nie powinien dowieść na podstawie znanych faktów oraz reguł. W trakcie wnioskowania hipoteza jest odkładana na **stos hipotez** w pamięci roboczej. Od tej pory moduł będzie próbował dowieść wszystkich hipotez znajdujących się na stosie, jeżeli na stosie znajduje się hipoteza, a nie da się dopasować żadnej reguły, to pierwotnie postawiona hipoteza jest fałszywa, w innym przypadku, jeżeli nie ma żadych reguł hipoteza jest prawdziwa. Sprawdza się prawdziwość tych hipotez poprzez dopasowywanie akcji, jeżeli zostanie dopasowana, to dokładamy do stosu wszystkie warunki elementarne reguły skłądające się na **poprzednik** reguły. Hipoteza może również być weryfikowana na podstawie faktów z pamięci roboczej. (przykład - str 135-136, podsumowanie str.137) 

