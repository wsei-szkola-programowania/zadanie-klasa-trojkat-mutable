---
Author: Krzysztof Molenda
Version:  0.1 (2019-02-05)
---

# Zadanie: klasa `Trojkat` _mutable_

Utwórz klasę `Trojkat` spełniającą następujące założenia:

1. Obiekt klasy `Trojkat` reprezentuje figurę geometryczną trójkąt, opisaną długościami trzech jej boków.

1. Obiekty klasy `Trojkat` są zmiennicze (_mutable_). Po utworzeniu, można zmieniać jego parametry (długości boków).

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

Napisz interaktywny program konsolowy weryfikujący funkcjonalność klasy `Trojkat`.

Przykładowy scenariusz:

1. Program prosi o podanie trzech długości boków.

2. Jeśli podane dane nie są numeryczne, zgłasza wyjątek i kończy pracę.

3. Tworzony jest obiekt typu `Trojkat` o zadanych bokach.

4. Wypisywane są na konsolę parametry trójkąta (obwód, pole, czy prostokątny, ostrokątny lub rozwartokątny).

5. Jeśli trójkąt jest równoramienny lub równoboczny, stosowna informacja wypisywana jest na konsolę.

