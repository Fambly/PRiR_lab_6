# PRiR_lab_6
Program MPI gra w życie. Posiłkując się programem dostarczonym do instrukcji sprawozdania należało opisać problem, strukturę programu i uzyskane wyniki.
# Problem: 
Gra w życie, stworzona przez Johna Conawaya polega na iteracyjnych zmianach stanów komórek. W zależności od ilości sąsiadów dana komórka ożywa, nie zmienia stanu lub umiera. Martwa komórka, która ma dokładnie 3 żywych sąsiadów staje się żywa w następnej iteracji. Żywa komórka z 2 albo 3 żywymi sąsiadami pozostaje nadal żywa; przy innej liczbie sąsiadów umiera (z „samotności” albo „zatłoczenia”)
# Struktura programu: 
Definiujemy na początku pliku górną granicę iteracji jako zmienna "DEFAULT_ITERATIONS", pola naszej 'planszy' do gry w życie oraz jej wysokość i szerokość (zakładamy że plansza jest kwadratowa). W main'ie inicjujemy naszą planszę, gdzie 1 to komórki żywe, a 0 to komórki martwe. Funkcja assert sprawdza czy podana ilość wątków które podał użytkownik jest podzielna przez liczbę kolumn/wierszy, jeśli spełniony jest ten warunek tworzona jest tablica lokalna, która będzie tymczasową kopią naszej planszy i stanu komórek jakie na niej są. Wykonywane będą tam operacje sprawdzania stanu komórek na następną iterację. Następnie nadpisujemy planszę główną wartościami z wyliczonymi stanami komórek z tymczasowej tablicy i wypisujemy wyniki. Operację tę powtarzamy do uzyskania porządanej liczby iteracji.
# Uzyskane wyniki: 
W zależności od podanej konfiguracji wartości 0 lub 1 zmieniają się, w przypadkach skrajnych 'przechodzą' one, tzn jeśli jesteśmy na najniższym polu planszy, a komórka powinna być jeszcze poniżej, to przechodzi ona do góry, analogicznie wygląda to w sytuacji lewo-prawo. W przypadku uruchomienia w wersji jaka jest podana domyślnie powinien wyjść wynik:
Iteration 63: final grid:

0  1  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  1  0  0  0  0  0  0  0  0  0  0  0  0  0  
1  1  1  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  0  
