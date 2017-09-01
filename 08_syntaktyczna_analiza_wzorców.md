# Syntaktyczna analiza wzorców

W tej metodzie wnioskowania dokonoju się na podstawie struktur opisujących świat zewnętrzny. Zbiór struktur/wzorców odpowiada bazie wiedzy. Zbiór taki nie jest zapisany w bazie wiedzy bezpośrednio, ale za pomocą systemu generującego wszystkie wzorce tego zbioru, tzw gramatyki generatywnej.

## 1) Generowanie reprezentacji strukturalnych

Aby skonstruować **gramatykę generatywną** potrzebny jest **zbiór symboli(etykiet) terminalnych**, z którego będziemy budować zdania należące do tego języka. Po prostu słowa, z których powstaną zdania.

**Produkcje** - są to reguły przepisujące (przykład na str.108 8.1, 8.2), są w nich **symbole pomocnicze (nieterminalne)**. Produkcje składają się z **lewej strony produkcji** oraz **prawej strony produkcji**. Zastosowanie produkcji polega na podmianie w frazy tożsamej z lewą stroną produkcji na prawą stronę. Sekwencja zastosowanych produkcji dążąca do wygenerowania danego zdania nazywana jest **wywodem/wyprowadzeniem** tego zdania, które składa się z **kroków wywodu**.

Istnieje również **zbiór symboli terminalych**. Gdy definiujemy gramatykę wyróżniony jest symbol nieterminalny od którego zaczynamy generowanie zdań, nazywa się on **symbolem startowym (etykietą startową lub aksjomatem)** i jest oznazany literką S. Istnieje również **słowo puste**.

Istnieje wiele rozdajów klas gramatyk generatywnych, można je ułożyć w hierarchię według kryterium **mocy generacyjnej (opisowej)**. Rodzaje gramatyk ze względu na moc obliczeniową:
- **gramatyka regularna** - pozwala jedynie doklejać symbol na końcu wyprowadzonego wyrażenia ( najsłabsza generacyjnie gramatyka)
- **gramatyka bezkontekstowa** - nie wprowadzają żadnych ograniczeń poza tym, że po lewej stronie musi się znajdować pojedyńczy symbol terminalny.

## 2)
