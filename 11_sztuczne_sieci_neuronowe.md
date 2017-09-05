# Sztuczne sieci neuronowe

## 1) Sztuczny neuron

**Sieć neuronowa** jest (bardzo uproszczonym) modelem struktury mózgu opartym na modelu **sztucznego neuronu** (str 160. rys 11.1) Sygnaly wejściowe odpowiadają impulsom nerwowym przesyłanym przez inne neurony. Aby obliczyć całkowitą siłę oddziaływania na neuron korzysta się z **funkcji potencjału postsynaptycznego**, u nas jest to *suma*. Sumaryczną siłę pobudzeniową potencjału postsynaptycznego obliczamy mnożąc sygnały wejściowe przez **wagi synaptyczne** a później je sumując. Po obliczeniu takiej sumy mozęmy sprawdzić, czy osiągnęła ona wartość progową neurony i czy został aktywowany, robi się to za pomocą **funkcji aktywacji**, która generuje sygnał wyjściowy.

Najprostsza funkcja aktywacji, to **funkcja skokowa heavisided'a**, oznaczana 1(v), która dla v < 0 przyjmuje 0, a dla v>=0 przyjmuje 1. (str. 162 rys. 11.2). 

Sieci neuronowe są zdolne do uczenia, chcemy aby neuron nauczył się reagować odpowiednio na pokazane mu wzorce. Ideą uczenia neuronu jest koregowanie jego wag w zależności od jego reakcji na pokazany wzorzec.

Po pokazaniu wszystkich wzorców neuronowi możemy sprawdzić, czy został on poprawnie nauczony tzn. sprawdzamy, czy poprawnie reaguje na zadane mu wzorce, jeżeli tak, to został nauczony, w przeciwnym wypadku musimy powtórzyć cały proces.

Istnieją dwie metody uczenia się neuronów:
- **uczenie z nauczycielem** - dla niego ciąg uczący jest postaci jak (str. 163 wzór 11.4) tzn. jest to wektor par - (wektor wejściowy, oczekiwana odpowiedź). Powinien dojść do moemntu w którym dla zadanych wektorów zwraca z niewielkim błędem oczekiwaną odpowiedź.
- **uczenie bez nauczyciela** - wektor postaci (str. 163 wzór 11.5), w tym przypadku powinien samodzielnie zmodyfikować swoje wagi tak aby dla podobnych wzorców generować taki sam sygnał wyjściowy, a dla niepodonych różne sygnały wyjściowe.

Ogólny schemat uczenia się neuronu (str. 163 rys. 11.3)

**Bipolarna funkcja skokowa** dla v <= -1 przyjmuje 0, a dla v>0 przyjmuje 1. (str. 164 rys. 11.4). 

nowe wagi = stare wagi + (wektor wejściowy * oczekiwany sygnał wyjściowy)

**Perceptron** to pojedyńczy neuron z bipolarna funkcja skokowa (str. 165 rys. 11.5a)

Sztuczne neurony mogą się różnić ze względu na:
- **Strukturalny schemat funkcjonalny** - inaczej wygląda dla **Adaline** (str. 167 rys. 11.7)
- **metoda uczenia** - inaczej wygląda dla Adaline, tam dodatkowo wykorzystywany jest współczynnik uczenia (str. 167 wzór. 11.8) **Reguła uczenia Hebba** jest to wzór w którym uwzględnia się aktywność poprzedniego neuronu w celu skorelowania ich aktywności (str. 168 wzór. 11.9)
- **postać funkcji aktywacji** :
  - **obcięta funkcja liniowa** (str. 169 wzór. 11.10)
  - **funkcja sigmoidalna** (str. 169 rys. 11.11)

## 2) Podstawowe rodzaje struktur sieci neuronowych

(rysunki na str. 170)

Najprostrzą siecią neuronową jest **sieć jednowarstwowa**. W strukturze **sieci wielowarstwowej** nerony warstw r przekazują sygnały do warstwy r+1. Pierwsza warstwa nazywana jest **warstwą wejściową**, ostatnia - **warstwą wyjściową**, a warstwy pomiędzy nazywane są **warstwami ukrytymi**. Sieci w których sygnały płyną w jednym kierunku nazywamy **sieciami jednokierunkowymi**. 

Podstawową metodą uczenia jednokierunkowej sieci wielowarstwowej jest **metoda wstecznej propagacji**. Na początku obliczamy sygnały wyjściowe dla ostaniej warstwy, potem obliczamy błąd zgodnie z odpowienidm wzorem (str. 171 wzór 11.14) , następnie propagujemy błąd wstecz zgodnie ze wzorem (str. 172 wzór 11.14), po czym obliczamy dla każego z neuronów nowe wagi (str. 173 wzór 11.16). (rysunki na str. 172)

Sieci zawierające połączenia do neuronów warstw wcześniejszych nazywamy **sieciami rekurencyjnymi**, przykładowe sieci:
- **sieć Hopfielda** - jednowarstwowa sieć, sygnał krąży po sieci aż sygnał wyjściowy nie przestanie się zmieniać
- **sieci Jordana** - posiada dodatkowow *neurony stanu*
- **sieci Elmanna** - podobne do *sieci Jordana*

## 3) Przegląd modeli sieci neuronowych

**Sieci pamięci skojarzeniowej (asocjacyjnej)** - służą do zapamiętywania wektorów wzorcowych w celu późniejszego rozpoznawania podobnych wektorów przez mechanizm skojarzenia. Najbadziej znane modele:
- dwuwarstwowa, jednokierunkowa, uczona z nauczycielem **sieć Hintona**
- **sieć typu BAM (dwukierunkowa pamięć asocjacyjna)** - dwuwarstwowa wersja *sieci Hopfielda*, w której sygnały przebiegają w cyklach - raz w jedną raz w drugą stronę.
- **sieć Hamminga** - trójwarstwowa wersja *sieci Hopfielda*, w której zewnętrzne warstwy są jednokierunkowe, a warstwa środkowa jest rekurencyjna. Jej działanie opiera się na minimalizcji odległości Hamminga.

**Sieci samoorganizujące** - wykorzysytwane w analizie skupisk, które generują dyskretną reprezentacje, zwaną mapą, które pokazują skupiska wektorów ciągu uczącego. Stosuje się tutaj szczególny rodzaj uczenia zwany **uczeniem z konkurencją**. Mechanizm uczenia wyzerowuje wyjścia wszystkich neuronów poza wyjściem neuronu zwycięskiego, tzn. takiego dla którego odległość wektora wag od wektora pokazywanego jest najmniejsza. Następnie korygowane są wagi albo tylko zwycięskiego (typ **WTA - winner takes all**) albo są korygowane wagi zwycięskiego i jego sąsiadów (typ **WTM - winner takes most**).

**Sieci typu ART** służa do rozpoznawania obrazów. Zapobiega zapominaniu wzorców przez sieci, taki problem występjuje, gdy już nauczoną sieć chcemy czegoś douczyć. Jeżeli podczas uczenia się sieci, wzorzec który chemy dołączyć jest bardzo podobny do zapamiętanych już elementów jakiejś klasy, to jest dołączany do niej. Jeśli jednak nie jest, to sieci tworzy nowa klasę. W tego typu sieciach istnieje parametr, który określa jak bardzo powinniśmy uogólniać klasy.

**Probabilistyczne sieci neuronowe** klasyfikują one wzorce na podstawie funkcji gęstości prawdopodobieństwa dla poszczególnych klas. Przykładem jest **maszyna Boltzmanna**.

**Sieci radialnych funkcji bazowych(sieci RBF)** - zamiast jednej globalnej funkcji bazowej definiujemy funkcje aktywacji dla każdego neuronu z osobna.


