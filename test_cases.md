

# Test Cases

1. Utworzenie nowego pliku z tekstem i ponowne uruchomienie aplikacji i sprawdzenie czy plik ma poprawną zawartość.
2. Otworzenie istniejącego pliku i zapisanie pod inną nazwą.
3. Zamiana każdego wystąpienia "text" na "nowy" w pliku.
4. Edycja wielu plików w różnych oknach przy podziale wertyklanym.
5. Edycja wielu plików w różnych zakładkach.
6. Nagranie i użycie prostego makra.
7. Usunięcie kilku znaków przy pomocy trybu VISUAL BLOCK.
8. Napisanie skryptu (inoremap <C-x>D Wprowadzony text ze skrótu.) ze skrótem i wykonanie :source i sprawdzenie czy działa.
9. Użycie wbudowanego menu pomocy do znalezienia sposobu wyjścia z edytora.
10. Uproszczona nawigacja przy pomocy automatycznego powtarzania komend.




## 1. Utworzenie nowego pliku z tekstem i ponowne uruchomienie aplikacji i sprawdzenie czy plik ma poprawną zawartość.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Włączyć tryb INSERT klikając: `i`.
4. Wpisać: `Test text.`.
5. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
6. Zapisać plik pod nazwą plik1.txt wpisując: `:w plik1.txt` i akceptując enterem.
7. Wyjść z edytora wpisując: `:q` i akceptując enterem.
8. Otworzyć ponownie plik i sprawdzić jego zawartość wpisując w wiersz poleceń: `vim plik1.txt` i akceptując enterem.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
4. Pokaże się `Test text.` w lewym górnym rogu wiersza poleceń.
5. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
6. Zostatnie utworzony nowy plik o nazwie `plik1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
7. Edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń.
8. Otworzy się edytor z uwcześniej zapisaną zawartością.
```


## 2. Otworzenie istniejącego pliku i zapisanie pod inną nazwą.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć istniejący plik wpisując w wiersz poleceń: `vim plik1.txt` i akceptując enterem.
3. Zapisanie pliku pod nową nazwą wpisując: `:w plik2.txt` i akceptując enterem.
4. Wyjście z edytora wpisując: `:q` i akceptując enterem.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się edytor z zawartością pliku `plik1.txt`.
3. Zostatnie utworzony nowy plik o nazwie `plik2.txt` z tą samą zawartością co plik `plik1.txt`.
4. Edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń (np. bash).
```


## 3. Zamiana każdego wystąpienia "text" na "nowy" w pliku.

```
1. Utworzyć plik z wielokrotnym wystąpieniem słowa `text` w dowolnym edytorze tekstowym (np. nano lub notepad++) i zapisać go w pliku `plik3.txt`.
2. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
3. Otworzyć istniejący plik wpisując w wiersz poleceń: `vim plik3.txt` i akceptując enterem.
4. Zamienić `text` na `nowy` wpisując: `:%s/text/nowy/g` i akceptując enterem.
```

```
1. Powstanie plik z licznym wystąpieniem słowa `text`.
2. Otwarty wiersz poleceń.
3. Otworzy się edytor z zawartością pliku `plik3.txt` z licznym wystąpieniem `text`.
4. Każde wystąpienie słowa `text` zostało zamienione na `nowy`.
```


## 4. Edycja wielu plików w różnych oknach przy podziale wertyklanym.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Otworzyć plik o nazwie `plik4-1.txt` wpisując: `:e plik4-1.txt` i akceptując enterem.
4. Włączyć tryb INSERT klikając: `i`.
5. Wpisać: `Test text 1.`.
6. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
7. Zapisać plik wpisując: `:w` i akceptując enterem.
8. Otworzyć drugie okno z podziałem wertykalnym poleceniem: `:vs` i akceptując enterem.
9. Otworzyć w nim kolejny plik o nazwie `plik4-2.txt` poleceniem: `:e plik4-2.txt` i akceptując enterem.
10. Włączyć tryb INSERT klikając: `i`.
11. Wpisać: `Test text 2.`.
12. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
13. Zapisać plik wpisując: `:w` i akceptując enterem.
14. Zamknięcie wszystkich okien i wyjście z aplikacji wpisując: `:qa` i akceptując enterem.
```

```
1. Otwarty wiersz poleceń z powłoką bash.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. Zostatnie otwarty nowy pusty plik o nazwie `plik4-1.txt` (ponieważ nie istnieje, zostanie otwarty pusty plik).
4. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
5. Pokaże się `Test text 1.` w lewym górnym rogu wiersza poleceń.
6. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
7. Zostatnie utworzony nowy plik na dysku o nazwie `plik4-1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
8. Wiersz poleceń zostatnie podzielony na 2 równe pionowe części (2 okna) z otwartym plikiem `plik4-1.txt`.
9. Zostatnie otwarty nowy pusty plik o nazwie `plik4-2.txt` (ponieważ nie istnieje, zostanie otwarty pusty plik).
10. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
11. Pokaże się `Test text 2.` w lewym górnym rogu wiersza poleceń, czyli w lewym oknie.
12. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
13. Zostatnie utworzony nowy plik na dysku o nazwie `plik4-1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
14. Oba okna edytora się zamknął, or edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń (np. bash).
```


## 5. Edycja wielu plików w różnych zakładkach.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Otworzyć plik o nazwie `plik5-1.txt` wpisując: `:e plik5-1.txt` i akceptując enterem.
4. Włączyć tryb INSERT klikając: `i`.
5. Wpisać: `Test text 1.`.
6. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
7. Zapisać plik wpisując: `:w` i akceptując enterem.
8. Otworzyć nową zakładkę poleceniem: `:newtab` i akceptując enterem.
9. Otworzyć w niej kolejny plik o nazwie `plik5-2.txt` poleceniem: `:e plik5-2.txt` i akceptując enterem.
10. Włączyć tryb INSERT klikając: `i`.
11. Wpisać: `Test text 2.`.
12. Wyjść z trybu INSERT do trybu NORMAL klikając ESC.
13. Zapisać plik wpisując: `:w` i akceptując enterem.
14. Zamknięcie wszystkich zakładek i wyjście z aplikacji wpisując: `:qa` i akceptując enterem.
```

```
1. Otwarty wiersz poleceń z powłoką bash.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. Zostatnie otwarty nowy pusty plik o nazwie `plik5-1.txt` (ponieważ nie istnieje, zostanie otwarty pusty plik).
4. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
5. Pokaże się `Test text 1.` w lewym górnym rogu wiersza poleceń.
6. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
7. Zostatnie utworzony nowy plik na dysku o nazwie `plik5-1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
8. W lewym górnym rogu pokażą się dwie zakładki, pierwsza z napisem `plik5-1.txt`, oraz druga `[No Name]`, która jest aktywna, oraz z brakiem zawartości.
9. Zostatnie otwarty nowy pusty plik o nazwie `plik5-2.txt` (ponieważ nie istnieje, zostanie otwarty pusty plik). Zmieni się nazwa drugiej zakładki na `plik5-2.txt`.
10. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
11. Pokaże się `Test text 2.` w lewym górnym rogu wiersza poleceń, czyli w lewym oknie.
12. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
13. Zostatnie utworzony nowy plik na dysku o nazwie `plik5-1.txt`, oraz pokaże się w lewym dolnym rogu nazwa pliku, oraz że został poprawnie zapisany.
14. Oba okna edytora się zamknął, or edytor się wyłączy, oraz będzie dostępny ponownie wiersz poleceń (np. bash).
```


## 6. Nagranie i użycie prostego makra do wypisywania copyright.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Nagrać makro wpisując: `qci// Copyright (C) 2022 Name<ESCAPE>q`, gdzie <ESCAPE> to klawisz escape.
4. Przejście do kolejnej linii klikając `o` i escape.
5. Uruchomić makro klikając: `@c`.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. W lewym górnym rogu wiersza poleceń pojawi się napis `// Copyright (C) 2022 Name`.
4. Kursor przeszedł na linię niżej i włączył się tryb INSERT, po czym przeszło do trybu NORMAL.
5. Pojawienie się drugiego takiego samego napisu `// Copyright (C) 2022 Name`.
```


## 7. Usunięcie kilku znaków przy pomocy trybu VISUAL BLOCK.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Przejście do trybu INSERT klikając: `i`.
4. Wpisanie dłuższej linijki, np: `Przykładowa dłuższa linijka do kilkukrotnego skopiowania.`.
5. Przejście do trybu NORMAL klikając escape.
6. Skopiowanie całej linijki kilkając: `yy`.
7. Dziesięciokrotne wklejenie skopiowanej linijki: `10p`.
8. Przejście na początek pliku klikając: `gg`.
9. Przejście w tryb VISUAL BLOCK klikając ctrl + v.
10. Poszerzenie zaznaczenia o kilka linijek w dół klikając 5 razy: `j`.
11. Poszerzenie zaznaczenia o kilka znaków w prawo klikając 5 razy: `l`.
12. Usunięcie zaznaczonego tekstu klikając: `x`.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
4. Pojawienie się dłuższej linijki w lewym górnym rogu wiersza poleceń.
5. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
6. Linijka została skopiowana do rejestru.
7. Pojawienie się dziesięciu kolejnych kopii wcześniej stworzonej linijki.
8. Kursor przeniesiony do lewego górnego rogu wiersza poleceń.
9. W lewym dolnym rogu wiersza poleceń pojawia się napis `-- VISUAL BLOCK --`.
10. Zaznaczenie powiększa się o 5 kolejnych wierszy.
11. Zaznaczenie poszerza się o 5 kolejnych kolumn.
12. Zaznaczony tekst zostaje usunięty.
```


## 8. Napisanie skryptu (inoremap <C-x>D Wprowadzony text ze skrótu.) ze skrótem i wykonanie :source i sprawdzenie czy działa.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć plik wpisując w wiersz poleceń: `vim plik8.txt` i akceptując enterem.
3. Przejście do trybu INSERT klikając: `i`.
4. Wpisanie skryptu ze skrótem klawiszowym klikając: `inoremap <C-x>D Tekst wypisany ze skrótu.`.
5. Wyjście z trybu INSERT do trybu NORMAL klikając escape.
6. Zapisanie pliku wpisując: `:w` i potwierdzając enterem.
7. Załadowanie wcześniej zapisanego pliku jako skryptu wpisując: `source plik8.txt`.
8. Otworzenie nowego pustego pliku wpisując: `:e new` i akceptując enterem.
9. Przejście do trybu INSERT klikając: `i`.
10. Użycie wcześniej przygotowanego skrótu klikając: ctrl + x i shift + d.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się edytor z pustym plikiem `plik8.txt`.
3. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
4. Pojawienie się w lewym górnym rogu `inoremap <C-x>D Tekst wypisany ze skrótu.`.
5. Nic widocznego się nie zmieni, jednak tryb zostatnie zmieniony na NORMAL.
6. Nowa zawartośc pliku została zapisana do pliku `plik8.txt`.
7. Nic widocznego się nie zmieni, jednak plik zostanie załadowany jako skrypt.
8. Nowy pusty plik o nazwie `new` zostaje otwarty.
9. W lewym dolnym rogu wiersza poleceń pojawi się napis `-- INSERT --`.
10. W lewym górnym rogu wiersza poleceń pojawi się napis `Tekst wypisany ze skrótu.`.
```


## 9. Użycie wbudowanego menu pomocy do znalezienia sposobu wyjścia z edytora.

```
1. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem.
2. Otworzyć edytor VIM poleceniem: `vim` i akceptując enterem.
3. Otworzyć menu pomocy dla wyjścia wpisując: `:help quit` i akceptując enterem.
4. Wyłączyć aktywne okno znalezionym poleceniem: `:quit` i akceptując enterem.
5. Powtórzyć poprzedni krok.
```

```
1. Otwarty wiersz poleceń.
2. Otworzy się aplikacja pokauzując wersję edytora na środku wiersza poleceń.
3. Okno aplikacji zostanie podzielone na pół i na jednek z połówek pokaże się menu pomocy z wypisanymi kilkoma poleceniami i ich opisami.
4. Okno pomocy zostanie zamknięte.
5. Aplikacja VIM zostaje zamknięta, oraz pokazują się spowrotem powłoka (np. bash).
```


## 10. Uproszczona nawigacja przy pomocy automatycznego powtarzania komend.

```
1. Znaleźć dowolny plik tekstowy, mający conajmniej 10 linijek tekstu i nazwać go `plik10.txt`.
2. Otworzyć wiersz poleceń z powłoką np. bash i zainstalowanym vimem w miejscu gdzie został zapisany plik `plik10.txt`.
3. Otworzyć istniejący plik wpisując w wiersz poleceń: `vim plik10.txt` i akceptując enterem.
4. Przejść do 9 linijki klikając: `9gg`.
5. Przejść 16 znaków w prawo klikając: `16l`.
6. Przejść 6 linijek do góry klikając: `6k`.
7. Usunąć 5 znaków klikając: `5x`.
```

```
1. Istnieje plik o nazwie `plik10.txt` tekstowy z zawartością conajmniej 10 linijek.
2. Otwarty wiersz poleceń.
3. Otworzy się edytor z zawartością pliku `plik10.txt`.
4. Kursor przeniesię się na początek 9 linijki.
5. Kursor przesunie się 16 znaków w prawo.
6. Kursor przesunie się 6 linijek do góry.
7. Zostanie usuniętych 5 kolejnych następujących po sobie znaków, zaczynając od znak na którym znajduje się kursor.
```


