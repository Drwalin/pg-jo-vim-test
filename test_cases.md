

# Test Cases

1. Utworzenie nowego pliku z tekstem i ponowne uruchomienie aplikacji i sprawdzenie czy plik ma poprawną zawartość.
2. Otworzenie istniejącego pliku i zapisanie pod inną nazwą.
3. Zamiana każdego wystąpienia "text" na "nowy" w pliku i zapisanie.
4. Edycja wielu plików w różnych oknach przy podziale wertyklanym.
5. Edycja wielu plików w różnych zakładkach.
6. Nagranie i użycie prostego makra.
7. Usunięcie kilku znaków przy pomocy trybu VISUAL BLOCK.
8. Napisanie skryptu (inoremap <C-x>D Wprowadzony text ze skrótu.) ze skrótem i wykonanie :source i sprawdzenie czy działa.





## 1. Utworzenie nowego pliku z tekstem i ponowne uruchomienie aplikacji i sprawdzenie czy plik ma poprawną zawartość.

1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Włączyć tryb INSERT klikając: `i`.
4. Wpisać: `Test text.`.
5. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
6. Zapisać plik pod nazwą plik1.txt wpisując: `:w plik1.txt` i akceptując enterem.
7. Wyjść z edytora wpisując: `:q` i akceptując enterem.
8. Otworzyć ponownie plik i sprawdzić jego zawartość wpisując w wiersz poleceń: `vim plik1.txt` i akceptując enterem.

1. Otwarty wiersz poleceń.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. W lewym dolnym rogu ekranu pojawi się napis `-- INSERT --`
4. Pokaże się `Test text.` w lewym górnym rogu wiersza poleceń.
5. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
6. Zostatnie utworzony nowy plik o nazwie `plik1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
7. Edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń.
8. Otworzy się edytor z uwcześniej zapisaną zawartością.


## 2. Otworzenie istniejącego pliku i zapisanie pod inną nazwą.

1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć istniejący plik wpisując w wiersz poleceń: `vim plik1.txt` i akceptując enterem.
3. Zapisanie pliku pod nową nazwą wpisując: `:w plik2.txt` i akceptując enterem.
4. Wyjście z edytora wpisując: `:q` i akceptując enterem.
5. Sprawdzenie czy istnieje plik z `plik2.txt` z zawartością pliku `plik1.txt`.

1. Otwarty wiersz poleceń.
2. Otworzy się edytor z zawartością pliku `plik1.txt`.
3. Utworzony nowy plik o nazwie `plik2.txt` z tą samą zawartością co plik `plik1.txt`.
4. Edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń.
5. 


## 3. Zamiana każdego wystąpienia "text" na "nowy" w pliku i zapisanie.



## 4. Edycja wielu plików w różnych oknach przy podziale wertyklanym.



## 5. Edycja wielu plików w różnych zakładkach.



## 6. Nagranie i użycie prostego makra.



## 7. Usunięcie kilku znaków przy pomocy trybu VISUAL BLOCK.



## 8. Napisanie skryptu (inoremap <C-x>D Wprowadzony text ze skrótu.) ze skrótem i wykonanie :source i sprawdzenie czy działa.





