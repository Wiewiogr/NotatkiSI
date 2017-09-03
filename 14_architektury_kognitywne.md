# Architektury kognitywne

**Architektura kognitywna** jest modelem informatycznym odpowiadającym *modelowii kognitywnemu*.

## 1) Koncepcja agenta

**Agent** to system, który **autonomicznie** reaguje na otoczenie na podstawie zebranych o nim informacji w konkretnym wyznaczonym celu. Deyzje agenta powinny być poparte **własnym doświadczeniem**, agent powienien mieć zdolność **uczenia się**.

Agent powinien posiadać meta wiedzę, możliwość percepcji, możliwość zapamiętywania oraz umiejętność wykonania pewnych czynności aby był w stanie się czegoś nauczyć.

Bardzo ważna jest *autonomiczność* agenta, tzn. to, że sam do wszystkiego dochodzi.

## 2) Systemy wieloagentowe

Systemy, w któreych działają zespoły agentów nazywamy **systemami wieloagentowymi**, wyróżnia się cztery ich podstawowe cechy:
- żaden agent nie dysponuje samodzielnie możliwością rozwiązywania problemów danej klasy,
- system nie jest sterowany centralnie,
- występuje rozproszenie informacji w systemie,
- obliczenia są realizowane w systemie w sposób asynchroniczny

Sposoby komunikowania się pomiędzy agentami:
- **architektura tablicowa** - agenci komunikują się między sobą wpisując różne informacje do globalnej tablicy. Agenci mogą być nazywani w niej *źródłami wiedzy*, może również istnieć *koordynator*, który zwraca uwagę agentów na to np. którym problemem powinni się teraz zająć. Tablica często ma strukturę hierarchii abstrakcji, gdzie na dole agneci obserwują fizyczny stan systemów, a Ci wyżej jakieś bardziej abstrakcyjne rzeczy.

  Rodzaje agentów w architekturze tablicowej:
  - **agent uwarunkowany odruchem** - *percepcja - akcja*
  - **agent uwarunkowany obserwacją** - obserwuje zachowania systemu w czasie i na tej podstawie może podejmować akcje
  - **agent uwarunkowany celem** - powinien wyznaczyć sobie cel na podstawie obserwacji agentów niżej w hierarchi

- **model przekazywania komunikatów** - agenci porozumiewają się za pomocą komunikatów.
