# Algorytm Bellmana-Forda

## Opis projektu
Ten projekt implementuje **algorytm Bellmana-Forda**, który służy do znajdowania najkrótszych ścieżek w grafie skierowanym, nawet w obecności ujemnych wag krawędzi. Program pobiera dane wejściowe z plików tekstowych i zwraca wynik w postaci pliku wyjściowego.

## Funkcjonalność
- Wczytywanie grafu z pliku tekstowego
- Obsługa ujemnych wag krawędzi
- Wykrywanie ujemnych cykli w grafie
- Zapis wyników do pliku
- Obsługa parametrów z linii poleceń

## Wymagania
- **Język programowania**: C++
- **Standard**: C++11 lub nowszy

## Struktura danych
Graf jest reprezentowany jako **lista sąsiedztwa**, gdzie każdy wierzchołek przechowuje swoje wychodzące krawędzie wraz z ich wagami. Dodatkowo wykorzystywane są mapy do kodowania indeksów wierzchołków.

## Uruchamianie programu
Program uruchamia się z linii poleceń, przekazując nazwy plików wejściowych i wyjściowych:
```bash
program -g graf.txt -w startowe.txt -o wynik.txt
```
### Opis parametrów:
- `-g` – plik wejściowy zawierający graf
- `-w` – plik zawierający wierzchołki startowe
- `-o` – plik wyjściowy z wynikami

Przykład uruchomienia:
```bash
./program -g input_graph.txt -w start_nodes.txt -o output.txt
```
Jeśli program zostanie uruchomiony bez parametrów lub z błędnymi argumentami, wyświetli pomoc.

## Algorytm
Algorytm Bellmana-Forda wykonuje **O(|V| × |E|)** operacji, gdzie **V** to liczba wierzchołków, a **E** to liczba krawędzi. Kroki działania:
1. Inicjalizacja odległości od wierzchołka startowego do wszystkich innych jako nieskończoność (∞), a do siebie jako 0.
2. Relaksacja wszystkich krawędzi **|V|-1** razy.
3. Sprawdzenie, czy występują ujemne cykle – jeśli tak, algorytm zwraca błąd.

## Struktura programu
- **`main.cpp`** – główna funkcja sterująca
- **`graph.h / graph.cpp`** – implementacja grafu i algorytmu Bellmana-Forda
- **`utils.h / utils.cpp`** – funkcje pomocnicze do obsługi plików i konwersji danych

## Testowanie
Program został przetestowany na różnych zestawach danych:
- Grafy poprawne (z i bez ujemnych wag)
- Grafy z ujemnymi cyklami (wykrywanie i obsługa błędu)
- Grafy z pustymi plikami wejściowymi

## Wnioski
Projekt pozwolił na zdobycie doświadczenia w:
- Implementacji algorytmów grafowych w C++
- Obsłudze plików wejściowych i wyjściowych
- Tworzeniu dokumentacji kodu (Doxygen)
- Pracy z systemem kontroli wersji **GitHub**

## Autor
Dawid Kosiński
