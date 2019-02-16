---
Author: Krzysztof Molenda
Version:  0.1 (2019-02-05)
---

# Zadanie: klasa `TrojkatM` _mutable_

Utwórz klasę `TrojkatM` spełniającą następujące założenia:

1. Obiekt klasy `TrojkatM` reprezentuje figurę geometryczną trójkąt, opisaną długościami trzech jej boków.

1. Obiekty klasy `TrojkatM` są zmiennicze (_mutable_). Po utworzeniu, można zmieniać jego parametry (długości boków).

1. Trójkąt domyślny, to taki, o bokach o długościach 1.

1. Należy dostarczyć funkcjonalności:
    * Wyliczenie pola powierzchni.
    * Wyliczenie obwodu.
    * Zwrócenie informacji, czy trójkąt jest prostokątny, rozwartokątny, ostrokątny.
    * Zwrócenie informacji, czy trójkąt jest równoboczny, czy jest równoramienny.
    * Eksport do postaci tekstowej.
    * Skalowania trójkąta (proporcjonalna zmiana jego wszystkich długości boków).

1. UWAGA:
    * W sytuacji podania niedodatnich długości boków, obiekt nie może powstać - zgłoszenie wyjątku `ArgumentOutOfRangeException`.
    * Nie dla każdych podanych długości trzech boków można utworzyć trójkąt - muszą spełniać tzw. warunek trójkąta. W takiej sytuacji zgłoszenie wyjątku `ArgumentException`.
    * Pole powierzchni trójkąta, przy zadanych długościach boków, można obliczyć ze [wzoru Herona](https://pl.wikipedia.org/wiki/Wz%C3%B3r_Herona).
    * Przy próbie zmiany długości któregokolwiek boku należy zweryfikować poprawność wprowadzanych danych i czy nowa wartość nie zaburza warunku istnienia trójkąta.

1. Napisz testy jednostkowe weryfikujące **wszystkie** publiczne funkcjonalności klasy.

---

Napisz interaktywny program konsolowy weryfikujący funkcjonalność klasy `TrojkatM`.

Przykładowy scenariusz:

1. Program prosi o podanie trzech długości boków.

2. Jeśli podane dane nie są numeryczne lub nie spełniają warunku trójkąta, zgłaszany jest odpowiedni wyjątek i program kończy pracę.

3. Tworzony jest obiekt typu `TrojkatM` o zadanych bokach.

4. Wypisywane są na konsolę parametry trójkąta (obwód, pole, czy prostokątny, ostrokątny lub rozwartokątny).

5. Jeśli trójkąt jest równoramienny lub równoboczny, stosowna informacja wypisywana jest na konsolę.

6. Program prosi o zmianę długości boku `a` (analogicznie dla `b` oraz `c`).

7. Jeśli podana wartość nie jest numeryczna lub zaburza warunek trójkąta, przechwytywany jest odpowiedni wyjątek i zmiany długości boku nie są wykonywane. Program kontynuuje pracę.

8. Jeśli dane są poprawne, program wypisuje na konsolę informacje o trójkącie po zmianach.

9. Program prosi o podanie współczynnika skali. Jeśli jest on poprawny (dodatni), trójkąt ulega przeskalowaniu. Jeśli jest niepoprawny, przechwytywane są zgłaszane wyjątki zaś skalowanie nie dochodzi do skutku.

10. Program wypisuje na konsolę informacje o trójkącie po zmianach.