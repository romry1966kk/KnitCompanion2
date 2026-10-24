# Knit Companion v 2.0 (C)2026

Autor: Marta Matulewicz

Program do pracy nad detalami na drutach: przechowuje wzory (np. warkocz, kwiatek) i pomaga śledzić, w którym rzędzie jesteś i co robić dalej. Działa w przeglądarce na iPadzie, iPhonie i Macu. Cały program to jeden plik `index.html`.

## Adres programu

[wpisz adres strony, np. https://nazwa.github.io/KnitCompanion2/]

Adres musi pozostać stały. Dane zapisują się w przeglądarce i są przypisane do adresu, więc po jego zmianie program będzie pusty (patrz „Kopia zapasowa”).

## Jak korzystać

Program ma trzy zakładki:

- **Śledzenie**: wybierasz pracę i miejsce użycia wzoru (np. Prawy przód). Program pokazuje bieżący rząd, instrukcję i kilka następnych rzędów. Po wykonaniu rzędu naciskasz „Ukończyłam rząd”. „Cofnij rząd” wraca o jeden.
- **Wzory**: tworzysz wzór jako siatkę symboli (malowanie palcem lub myszką), wpisujesz instrukcje do rzędów i edytujesz słownik symboli. Wpisuj tylko rzędy po prawej stronie, rzędy powrotne program dodaje sam.
- **Prace**: tworzysz prace, dodajesz zdjęcie i miejsca użycia wzoru. Dla każdego miejsca ustawiasz wzór, tryb (płasko lub na okrągło), rząd, w którym wzór się zaczyna, rząd wzoru, od którego zaczynasz, oraz aktualny rząd. Tu jest też kopia zapasowa.

Czerwona plakietka **OFFLINE** pokazuje, że urządzenie nie ma połączenia z internetem.

## Gdzie są zapisane dane

Wszystkie wzory, prace i zdjęcia zapisują się **w przeglądarce na danym urządzeniu**. Nie są wysyłane na żaden serwer. Oznacza to, że:

- iPad, iPhone i Mac mają osobne dane,
- wyczyszczenie danych stron w przeglądarce kasuje prace,
- inna przeglądarka na tym samym urządzeniu ma własne, puste dane.

## Kopia zapasowa

Rób ją regularnie, a zawsze przed zmianą adresu programu lub przeniesieniem folderu:

1. Zakładka **Prace** → **Zapisz do pliku**.
2. Zapisz plik w aplikacji Pliki, najlepiej w iCloud Drive.
3. Aby wczytać, w tej samej zakładce użyj **Wczytaj z pliku**. Wczytanie zastępuje wszystkie dane na urządzeniu.

W ten sposób przenosisz też prace między urządzeniami lub osobami. To kopia, a nie synchronizacja: zmiany po obu stronach nie scalają się same.

## Zmiana ustawień w kodzie

Na początku skryptu w `index.html` jest blok `USTAWIENIA` z tytułem, autorem, limitami rozmiaru wzoru, liczbą rzędów w podglądzie, tekstami rzędów pośrednich i domyślnym słownikiem symboli. Każda pozycja ma komentarz po polsku.

Uwaga: nie zmieniaj wartości `klucz`, jeśli ktoś już używa programu, bo praca zniknie z widoku. Jeśli chcesz testować na osobnych danych, użyj w testowej kopii innego klucza.

## Testowanie zmian

Zmiany sprawdzaj najpierw lokalnie: otwórz `index.html` dwuklikiem na Macu. Dane lokalne są osobne od danych na stronie w internecie. Przed przeniesieniem folderu w inne miejsce zrób kopię zapasową.

## Struktura repozytorium

```
index.html    cały program
README.md     ten plik
```

## Ważne

- To repozytorium jest publiczne. **Nie wrzucaj tu kopii zapasowych ani zdjęć swoich prac.**
- Program jest udostępniany bez gwarancji. Autor nie odpowiada za utratę danych, dlatego rób kopie zapasowe.
- Licencja: wszelkie prawa zastrzeżone.
