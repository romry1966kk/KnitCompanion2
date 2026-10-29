# Knit Companion v 2.0

© 2026 Marta Matulewicz

Program do śledzenia postępu robótki na drutach. Przechowuje wzory (np. warkocz, kwiatek), a podczas dziergania pokazuje, w którym rzędzie jesteś i co robić dalej. Działa w przeglądarce na iPadzie, iPhonie i Macu. Cały program to jeden plik `index.html`.

## Adres programu

https://romry1966kk.github.io/KnitCompanion2/

Adres musi pozostać stały. Dane zapisują się w przeglądarce i są przypisane do adresu, więc po jego zmianie program będzie pusty (patrz „Zapis i kopia zapasowa”).

## Jak korzystać

Program ma cztery zakładki: Śledzenie, Projekt, Ustawienia i Prompt.

### Śledzenie

- Z listy wybierasz **wzór** (np. „Warkocz - prawy przód”).
- Widzisz zdjęcie projektu, **panel z instrukcją** aktywnego rzędu (wpisaną w zakładce Projekt) i **tabelę** kilku następnych rzędów. Pod tabelą jest legenda symboli użytych w tym wzorze.
- Po lewej stronie tabeli, przy aktywnym rzędzie, jest ikona jego rodzaju: **➡ normalny**, **↩ powrót** (tryb płasko, rzędy parzyste) albo **🔄 na okrągło**. Przy rzędzie powrotnym panel zaczyna się od „Powrót:” (dopisuje to program, w instrukcji wpisujesz tylko resztę).
- **Pole Info** pod tabelą i legendą symboli („Informacja dla tego rzędu”) to miejsce na krótką notatkę techniczną przypisaną do numeru licznika, np. „-2” albo „+10” (zmniejszanie i dodawanie oczek w rękawie). Pokazuje i zmienia notatkę tylko aktywnego rzędu, zapisuje się od razu i nie wywołuje żadnych pytań. Puste pole usuwa notatkę, a duży przycisk **Del** po prawej stronie robi to jednym dotknięciem, bez klawiatury. Rzędy, które mają notatkę, są w tabeli oznaczone po lewej ikoną „i” (od chwili, gdy wejdą do podglądu), a sama treść pokazuje się dopiero przy aktywnym rzędzie. Po zmianie notatek pod polem pojawia się żółte, wyciszone przypomnienie o zapisie projektu do pliku; znika po zapisie (nie znika, jeśli klikniesz Anuluj).
- **Duży numer** to licznik rzędu tego wzoru. Przyciski **Ukończono rząd** i **Cofnij rząd** zmieniają go o jeden. Dotknięcie numeru pozwala wpisać dowolny rząd.
- Wzór, który nie jest „bez końca”, zatrzymuje licznik na ostatnim rzędzie: przycisk „Ukończono rząd” jest wtedy nieaktywny, w panelu pojawia się wyróżniona jaśniejszym kolorem informacja „Koniec wzoru”, a pod tabelą widać (niepodświetlony) wiersz z ikoną **bez końca**. Kliknięcie ikony włącza powtarzanie wzoru i licznik liczy dalej.

### Projekt

- **Nazwa** projektu (tylko informacja; tworzenie, wczytywanie i usuwanie projektów jest w Ustawieniach) oraz opcjonalne **zdjęcie** projektu (.png, .jpg, .jpeg, .webp, .gif, .heic).
- **Wzory** projektu: **Nowy wzór**, **Duplikuj wzór** i **Usuń wzór**. Każdy wzór ma własny licznik, własną nazwę i tryb (**płasko** lub **na okrągło**, wybierany przyciskami) oraz co najmniej dwa rzędy. Ten sam wzór możesz zduplikować i nazwać inaczej (np. dla prawego i lewego przodu).
- **Edytor wzoru:** ustawiasz liczbę oczek (przyciski zmieniają o 1) i rzędów (przyciski zmieniają o 2, wzór ma zawsze parzystą liczbę rzędów, minimum 2), wybierasz symbol z palety i malujesz palcem lub myszką. Rząd 1 jest na dole, a kolejne rzędy rosną w górę, tak jak dzianina na drutach (w Śledzeniu tabela jest ułożona jak dotąd). **Rysujesz wszystkie rzędy, także powrotne**, a wzór powtarza się od pierwszego rzędu.
- **Telefon w pionie:** na wąskim ekranie dotykowym edycja tabeli wzoru jest zablokowana (komórki są za małe). Po dotknięciu tabeli pojawia się pasek z prośbą o obrócenie telefonu poziomo (jeśli ekran się nie obraca, trzeba wyłączyć blokadę obrotu). Próg szerokości jest w `USTAWIENIA` (`minSzerokoscEdycji`). Na komputerze i iPadzie blokady nie ma.
- **Instrukcje:** nad każdym rzędem tabelki jest pole na instrukcję (np. „Powrót: przerabiaj oczka tak, jak schodzą z drutu.”). Pojawia się w panelu w Śledzeniu, gdy ten rząd jest aktywny.
- **∞ rzędy bez końca** (przycisk pod wierszem z liczbą oczek i rzędów): podświetlony oznacza wzór powtarzany bez końca.
- **Kopiuj Info z...** (lista obok „rzędy bez końca”): każdy wzór ma własne notatki Info. Z listy możesz wybrać inny wzór (przy nazwie jest liczba jego notatek) i skopiować jego notatki do bieżącego wzoru, np. z rękawa pierwszego do drugiego. Kopiuje się tylko treść notatek. Jeśli bieżący wzór ma już własne notatki, program pyta, czy je zastąpić. Po skopiowaniu lista wraca na „—” (brak wyboru), a pod nią widać krótki komunikat. Kopiowanie nie zmienia rysunku wzoru. Duplikat wzoru dostaje własną kopię notatek, a usunięcie wzoru usuwa jego notatki (program o tym uprzedza).
- **Ostrzeżenie:** wzór z licznikiem większym niż 1 jest „w użyciu”. Zmiana takiego wzoru może zepsuć pracę, więc program pokazuje pasek ostrzeżenia i pyta przed zmianą. Do prób użyj **Duplikuj wzór**.

### Ustawienia

Sekcja **Zapis/Odczyt projektu: [nazwa projektu]** zawiera:

- **Zapisz dane projektu**: zapisuje cały projekt do pliku. Nazwa pliku to nazwa projektu oraz data i godzina.
- **Wczytaj dane projektu** (.json): wczytuje projekt z pliku i zastępuje bieżący. Program pyta o potwierdzenie (to samo przy resecie, nowym projekcie i usunięciu projektu; jeśli są notatki Info, pytanie przypomina, że zostaną utracone). Notatki Info zapisują się w pliku razem z projektem.
- **Reset do domyślnych**: zastępuje bieżący projekt przykładowym. Przykładowy projekt jest wbudowany w program i ma w nazwie dopisek „(domyślny)”. Przy pierwszej zmianie w zakładce Projekt (wzór, zdjęcie, słownik symboli) program pyta o zgodę i zmienia dopisek na „(zmieniony)”: od tej chwili to Twój projekt zapisany w przeglądarce. Zmiany w kodzie projektu domyślnego widać dopiero po „Reset do domyślnych”.
- **Nowy projekt**: wpisujesz nazwę i tworzysz pusty projekt.
- **Usuń projekt**: usuwa bieżący projekt z programu (zapisany wcześniej plik zostaje).

**Słownik symboli**: znak i nazwa każdego symbolu dostępnego w palecie. Słownik zapisuje się razem z projektem. Zmiana samego znaku zmienia sens narysowanych wzorów.

Czerwona plakietka **OFFLINE** informuje, że urządzenie nie ma połączenia z internetem. Pełna praca bez internetu nie jest jeszcze gwarantowana.

### Prompt

Zakładka pomaga przygotować polecenie (prompt) dla ChatGPT. Ma dwie osobne sekcje i każda zapisuje własny plik tekstowy (.txt):

- **Grafika wzoru**: wybierasz, co pokazać, kolor, wygląd i grubość włóczki, ujęcie i tło. Powstaje polecenie do wygenerowania poglądowej grafiki dzianiny. AI ma oddać samą grafikę, bez tekstu, komentarzy i pytań.
- **Szacunek włóczki**: podajesz rodzaj wyrobu i krój, rozmiar, wagę i metraż motka z etykiety, próbkę 10×10 cm (oczka i rzędy), udział wzorów i ewentualne uwagi. Powstaje polecenie o oszacowanie ilości włóczki. AI ma odpowiedzieć dwiema liniami z liczbami (minimum i z zapasem, w gramach, metrach i motkach), bez wyjaśnień. Wynik to szacunek, nie dokładne wyliczenie; w razie wątpliwości dopytaj w rozmowie.

Do każdego pliku program dokłada instrukcję, Twoje odpowiedzi (puste pola jako „nie podano”) oraz opis wszystkich wzorów projektu: oczka, rzędy zapisane znakami, instrukcje i legendę symboli. Plik dołącz do rozmowy z ChatGPT albo wklej jego treść. Zdjęcia projektu program do pliku nie dołącza, możesz dodać je do rozmowy osobno. Odpowiedzi z formularzy zapisują się razem z projektem (trafiają też do pliku .json) i nie wywołują pytania o zmianę projektu domyślnego.

## Gdzie są zapisane dane

Wszystkie wzory, projekt i zdjęcie zapisują się **w przeglądarce na danym urządzeniu**. Nie są wysyłane na żaden serwer. Oznacza to, że:

- iPad, iPhone i Mac mają osobne dane,
- wyczyszczenie danych stron w przeglądarce kasuje projekt,
- inna przeglądarka na tym samym urządzeniu ma własne, puste dane,
- strona otwarta z adresu w internecie i ten sam plik otwarty lokalnie z dysku to dwa osobne programy z osobnymi danymi.

W przeglądarce jest zawsze **jeden bieżący projekt**.

## Zapis i kopia zapasowa

Rób ją regularnie, zawsze przed wczytaniem innego projektu i przed zmianą adresu programu.

1. Zakładka **Ustawienia** → **Zapisz dane projektu**.
2. Na iPhonie i iPadzie otworzy się arkusz udostępniania: wybierz **Zapisz w Plikach** i folder (najlepiej w iCloud Drive). Na komputerze w Edge lub Chrome otworzy się okno zapisu, w którym możesz zastąpić istniejący plik.
3. Aby wczytać, w tej samej zakładce użyj **Wczytaj dane projektu**.

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
- Licencja: wszelkie prawa zastrzeżone. © 2026 Marta Matulewicz. Kod jest publicznie widoczny, ale nie wolno go kopiować, zmieniać ani rozpowszechniać bez zgody autorki.
