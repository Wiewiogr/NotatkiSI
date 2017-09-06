# Definiowanie pojęć nieostrych w systemach wiedzy

Problemy związane z **niedoskonałością aparatu pojęciowego**:
- **nieostre pojęcia**
  - **niejednoznaczność** (np. wiek, czy stary, czy młody)
  - **stopień szczegółowości**
  
## 1) Model oparty na zbiorach rozmytych

**Uniwersum rozważań** jest zbiorem interesujących nas elementów.

**Pojęcie ostre** to takie, w którym zawsze można rozróżnić elementy objęte tym pojęciem.

**Pojęcie nieostre** to takie, które nie jest określone w sposób jednoznaczny.

W **teorii zbiorów rozmytych** przynależność do zbiorów jest funkcją, która przyjmuje wartości od 0 do 1. Jeżeli w zbiorach występuję właśnie taka **częściowa przynależność**, to taki zbiór nazywamy **zbiorem rozmytym**.

**Zmienna lingwistyczna** to taka zmeinna, której w zależności od jej wartości przypisujemy jej jakieś **wartości lingwistyczne**. Np. Wiek, to *zmienna lingwistyczna*, której w zależności od ilości lat przypiszemy jakieś *wartości lingwistyczne* np. młody, stary. Odwzorowanie, które przyporządkowuje *wartości lignwistycznej* zbiór rozmyty, to **funkcja semantyczna**.

### Logika rozmyta

Różnica pomiędzy **logiką rozmytą** a klasyczną jest taka, że w klasycznej przyjmowane są jedynia wartości *Prawda* i *Fałsz*, a w *rozmytej* mogą to być wartości z przedziału [0,1]. W logice rozmytej wykorzystywana jest **funkcja stopnia prawdy**, w tej funkcji bierzemy mniejszą wartość z tych, które nas interesują np. jeżeli chcemy sprawdzić jak jak bardzo jesteśmy Młodzi i Dojrzali mając 25 lat, to bierzemy mniejszą wartość spośród stopnia dojrzałości i młodości dla 25 lat.

### Rozmyty system regułowy

Zarówno w części *COND* jak i w *ACT* mogą pojawić się pojęcia nieostre. Etapy:
1. Obliczenie **stopnia spełnialności** *COND*
2. Wykorzstanie **formuły minimum w modelu wnioskowania Mamdaniego**. (???)
3. Dokonanie **agregacji konkluzji**. (???)
4. Wykonanie **operacji wyostrzania**, która zbiorowi rozmytemu przyporządkowuje wartość liczbową.

## 2) Model oparty na zbiorach przybliżonych

### Teoria zbiorów przybliżonych

#### dla pojęć ostrych

Poziom szczegółowości charakterystyki pojęcia powinien być *adekwatny* w stosunku do rozważanego problemu. Tzn. tyle, że w zależności od tego czego oczekujemy możemy tworzeć mniej lub bardziej szczegółowe rozwiązania. np. zamiast rozważać coś rozbitego na konkretne miasta w polsce, można by to uogólnić do województw i miast w zależności od naszych zapotrzebowań, robiąc coś takiego zwiększamy **granule wiedzy**. Gdy uogólniamy z miast do województw, to miasta z jednego województwa stają się **elemtami nierozróżnialnymi**.

#### dla pojęć nieostrych

**dolne przybliżenie** - zbiór, który na pewno jest objęty pojęciem.

**górne przybliżenie** - zbiór, który być może jest objęty pojęciem.

**brzeg zbioru** - różnica między dolnym, a górnym przybliżeniem

**zbiór przybliżony** to zbiór dla którego przy ustalonej granujacji uniwersum dolne przybliżenie jest różne od górnego

**zbiór dokładny** to zbiór dla którego dolne przybilżenie jest równe górnemu.

**Współczynnik dokładności aproksymacji zbioru** - mówi jak dobra jest aproksymacja dolnym i górnym przybliżeniem. Jest równy dzieleniu dolnego przybliżenia przez górne.


(str. 201-204)
