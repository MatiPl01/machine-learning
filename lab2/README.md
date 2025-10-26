# Laboratorium 2 - Interpretowalność modeli ML

## Przebieg laboratoriów

- Na początku krótki wstęp dot. poznawanych metod interpretowalności
- Na koniec zadanie domowe
- **Zadanie jest do zrobienia na zajęciach**
  - Da się je zrobić na zajęciach
  - Nie trzeba go skończyć na zajęciach - czas do wtorku 23:59

## Zadania do wykonania

### Część 1: Notebook lime_shap_tabular

- **Część I** (tylko LIME, bez SHAP!)
- W zadaniu domowym proszę wykorzystać **MLPClassifier** z biblioteki sklearn
- Zadbaj, żeby jakość predykcji była przynajmniej **akceptowalna** - najlepiej nie mniej niż **0.8**

### Część 2: Notebook lime_images

- Wybierz **własny** (inny niż amfibia) obraz z dowolnej klasy rozpoznawanej przez sieć
- Wykorzystaj obraz spoza zbioru ImageNet, na którym trenowana była sieć
- Wykonaj zadania 1 i 2, używając **dwóch** dowolnych pretrenowanych sieci neuronowych
- Jedną z nich może być wykorzystana w tutorialu sieć Inception

## Raport

- Raport proszę przygotować w formie tekstowej i zamieścić PDF
- **Raportem nie jest** uzupełniony notebook - proszę zrobić "tradycyjny" raport ze wszystkimi koniecznymi wnioskami i wykresami (!)
- Proszę pisać krótkie i samodzielne komentarze
- Oczekiwana długość raportu: **max 2 strony A4**, może być nieco dłuższy, jeśli będzie to konieczne ze względu na obrazki/wykresy

## Terminy i ocenianie

- Raporty przyjmuję do dwóch tygodni od terminu zajęć (7.11)
- Po terminie zadania (wtorek 23:59) wynik mnożony jest przez 0.7
- Po dwóch tygodniach **nie przyjmuję** już zadań
- W celu zaliczenia przedmiotu trzeba zaliczyć każde laboratorium, tj. uzyskać min. 50% punktów
- **UWAGA**: nie przewiduję na koniec semestru sprawdzania zadań osób, które nie zaliczyły wcześniej laboratorium!

## Zgłaszanie prac

- Proszę umieścić na Teamsie raport w PDF oraz uzupełniony notebook
- Ocenie podlega wyłącznie raport, notebook może (nie musi) być weryfikowany w przypadku wątpliwości

## Rozwiązywanie problemów technicznych

### Wyświetlanie obrazków

- W obu częściach powinny się Państwu wyświetlać obrazki
- Gdyby coś nie działało - proszę zmienić przeglądarkę
- W zeszłym roku był problem z wyświetlaniem w VS

### Problem z podziałem danych

Na niektórych platformach (jedna osoba zgłosiła problem na colabie) następował inny podział na dane treningowe i testowe niż w przygotowanym notebooku, pomimo pozostawienia tego samego ustawienia seeda.

**Rozwiązania:**

1. Zmienić platformę... lub
2. Znaleźć w zbiorze testowym podobne przykłady do tych analizowanych w notebooku, lub
3. Wyciągać dane ze zbioru "data", który u każdego wczytuje się tak samo, a nie ze zbioru testowego

**Indeksy wybranych przykładów względem zbiorów:**

- testowy w notebooku -> data:
  - 1653 -> 31216
  - 92 -> 6508
  - 18 -> 21145

Jako, że zbiory podzieliły się inaczej na treningowy i testowy niż w dostarczonym notebooku, te przykłady mogą być tłumaczone przez LIME'a inaczej, ale warto sprawdzić tę opcję.

Jak wszystko zawiedzie to analizować te przykłady, które się załadowały. Mogą być mniej ciekawe niż te wybrane :( więc niech to będzie faktycznie ostateczna opcja.

### Błąd importu IPython

Jeśli komuś wyrzuca błąd związany z importem IPython.core.display, należy wejść w zainstalowanego lime w plik wskazany w błędzie i zmienić import na `from IPython.display` (wyrzucić core).
