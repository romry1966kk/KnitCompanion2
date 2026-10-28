# Knit Companion v 2.0

© 2026 Marta Matulewicz

Program do śledzenia postępu robótki na drutach. Przechowuje wzory (np. warkocz, kwiatek), a podczas dziergania pokazuje, w którym rzędzie jesteś i co robić dalej. Działa w przeglądarce na iPadzie, iPhonie i Macu. Cały program to jeden plik `index.html`.

## Adres programu

https://romry1966kk.github.io/KnitCompanion2/

Adres musi pozostać stały. Dane zapisują się w przeglądarce i są przypisane do adresu, więc po jego zmianie program będzie pusty (patrz „Zapis i kopia zapasowa”).

## Jak korzystać

Program ma trzy zakładki.

### Śledzenie

- Z listy wybierasz **wzór** (np. „Warkocz - prawy przód”).
- Widzisz zdjęcie projektu, **panel z instrukcją** aktywnego rzędu (wpisaną w zakładce Projekt) i **tabelę** kilku następnych rzędów. Pod tabelą jest legenda symboli użytych w tym wzorze.
- Po lewej stronie tabeli, przy aktywnym rzędzie, jest ikona jego rodzaju: **➡ normalny**, **↩ powrót** (tryb płasko, rzędy parzyste) albo **🔄 na okrągło**. Przy rzędzie powrotnym panel zaczyna się od „Powrót:” (dopisuje to program, w instrukcji wpisujesz tylko resztę).
- **Duży numer** to licznik rzędu tego wzoru. Przyciski **Ukończyłam rząd** i **Cofnij rząd** zmieniają go o jeden. Dotknięcie numeru pozwala wpisać dowolny rząd.
- Wzór, który nie jest „bez końca”, zatrzymuje licznik na ostatnim rzędzie: przycisk „Ukończyłam rząd” jest wtedy nieaktywny, w panelu pojawia się wyróżniona jaśniejszym kolorem informacja „Koniec wzoru”, a pod tabelą widać (niepodświetlony) wiersz z ikoną **bez końca**. Kliknięcie ikony włącza powtarzanie wzoru i licznik liczy dalej.

### Projekt

- **Nazwa** projektu (tylko informacja; tworzenie, wczytywanie i usuwanie projektów jest w Ustawieniach) oraz opcjonalne **zdjęcie** projektu (.png, .jpg, .jpeg, .webp, .gif, .heic).
- **Wzory** projektu: **Nowy wzór**, **Duplikuj wzór** i **Usuń wzór**. Każdy wzór ma własny licznik, własną nazwę i tryb (**płasko** lub **na okrągło**, wybierany przyciskami) oraz co najmniej dwa rzędy. Ten sam wzór możesz zduplikować i nazwać inaczej (np. dla prawego i lewego przodu).
- **Edytor wzoru:** ustawiasz liczbę oczek i rzędów, wybierasz symbol z palety i malujesz palcem lub myszką. Rząd 1 jest u góry. **Rysujesz wszystkie rzędy, także powrotne**, a wzór powtarza się od pierwszego rzędu.
- **Instrukcje:** nad każdym rzędem tabelki jest pole na instrukcję (np. „Powrót: przerabiaj oczka tak, jak schodzą z drutu.”). Pojawia się w panelu w Śledzeniu, gdy ten rząd jest aktywny.
- **∞ rzędy bez końca** (przycisk pod wierszem z liczbą oczek i rzędów): podświetlony oznacza wzór powtarzany bez końca.
- **Ostrzeżenie:** wzór z licznikiem większym niż 1 jest „w użyciu”. Zmiana takiego wzoru może zepsuć pracę, więc program pokazuje pasek ostrzeżenia i pyta przed zmianą. Do prób użyj **Duplikuj wzór**.

### Ustawienia

Sekcja **Zapis/Odczyt projektu: [nazwa projektu]** zawiera:

- **Zapisz w Plikach**: zapisuje cały projekt do pliku. Nazwa pliku to nazwa projektu oraz data i godzina.
- **Wczytaj z pliku** (.json): wczytuje projekt z pliku i zastępuje bieżący. Program pyta o potwierdzenie.
- **Reset do domyślnych**: zastępuje bieżący projekt przykładowym.
- **Nowy projekt**: wpisujesz nazwę i tworzysz pusty projekt.
- **Usuń projekt**: usuwa bieżący projekt z programu (zapisany wcześniej plik zostaje).

**Słownik symboli**: znak i nazwa każdego symbolu dostępnego w palecie. Słownik zapisuje się razem z projektem. Zmiana samego znaku zmienia sens narysowanych wzorów.

Czerwona plakietka **OFFLINE** informuje, że urządzenie nie ma połączenia z internetem. Pełna praca bez internetu nie jest jeszcze gwarantowana.

## Gdzie są zapisane dane

Wszystkie wzory, projekt i zdjęcie zapisują się **w przeglądarce na danym urządzeniu**. Nie są wysyłane na żaden serwer. Oznacza to, że:

- iPad, iPhone i Mac mają osobne dane,
- wyczyszczenie danych stron w przeglądarce kasuje projekt,
- inna przeglądarka na tym samym urządzeniu ma własne, puste dane,
- strona otwarta z adresu w internecie i ten sam plik otwarty lokalnie z dysku to dwa osobne programy z osobnymi danymi.

W przeglądarce jest zawsze **jeden bieżący projekt**.

## Zapis i kopia zapasowa

Rób ją regularnie, zawsze przed wczytaniem innego projektu i przed zmianą adresu programu.

1. Zakładka **Ustawienia** → **Zapisz w Plikach**.
2. Na iPhonie i iPadzie otworzy się arkusz udostępniania: wybierz **Zapisz w Plikach** i folder (najlepiej w iCloud Drive). Na komputerze w Edge lub Chrome otworzy się okno zapisu, w którym możesz zastąpić istniejący plik.
3. Aby wczytać, w tej samej zakładce użyj **Wczytaj z pliku**.

W ten sposób przenosisz też projekt między urządzeniami lub osobami. To kopia, a nie synchronizacja: zmiany po obu stronach nie scalają się same.

## Zmiana ustawień w kodzie

Na początku skryptu w `index.html` jest blok `USTAWIENIA` z tytułem, numerem wersji, autorem, rokiem, limitami rozmiaru wzoru, liczbą rzędów w podglądzie, tekstami rzędów powrotnych i domyślnym słownikiem symboli. Każda pozycja ma komentarz po polsku.

Uwaga: nie zmieniaj wartości `klucz`, jeśli ktoś już używa programu, bo projekt zniknie z widoku. Do testów na osobnych danych użyj innego klucza.

## Aktualizacja programu (lista kontrolna autora)

1. Zmień numer w polu `wersja` w `USTAWIENIA`.
2. Wgraj plik na GitHub i poczekaj, aż w zakładce Actions pojawi się zielony znaczek.
3. Zamknij kartę i otwórz adres od nowa (albo odśwież twardo: Cmd+Shift+R na Macu, Ctrl+Shift+R na Windowsie). Zwykłe odświeżenie może pokazać starą wersję.
4. Sprawdź w stopce, czy numer wersji się zgadza.
5. Dopiero potem testuj zmianę.

Zmiany sprawdzaj najpierw lokalnie: otwórz `index.html` dwuklikiem. Dane lokalne są osobne od danych na stronie w internecie. Przed przeniesieniem folderu z plikiem w inne miejsce zrób kopię zapasową.

## Struktura repozytorium

```
index.html          cały program
img/domyslne.jpg    zdjęcie przykładowego projektu
README.md           ten plik
```

## Ważne

- To repozytorium jest publiczne. **Nie wrzucaj tu kopii zapasowych ani zdjęć swoich prac.**
- Program jest udostępniany bez gwarancji. Autor nie odpowiada za utratę danych, dlatego rób kopie zapasowe.
- Licencja: [uzupełnij]
