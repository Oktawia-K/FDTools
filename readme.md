# To jest ***bardzo*** ważny tytuł!
### Zasługuje na szacunek.

### Procedury Git

- git add [nazwy plików] / git add . (każdy zmieniony plik)
    - staging zmian
- git commit m"[wiadomość]"
- gitk
    - wizualna reprezentacja commitów i ich zmian
    - gitk -all
        - zmiana zakresu na wszystkie gałęzie
- git log
    - historia repo
    - git log --oneline
        - wygodniejszy wgląd w historię bez detali
- git diff
    - szybki podgląd zmian przed dodaniem do commita (nie wygodne przy obszernych zmianach)

---
- **tagi**
    - ==lightweight== - skrót SHA-1 commita
    - ==annotated== - dane autora, data, komentarz *i SHA-1* danego commita
        - git tag [nazwa] [numer_commit]
    - lightweight
        - `git tag "Wprowadzenie" 39f7004`
    - git tag [nazwa] [numer_commit] -a -m"[komentarz]"
    - annotated
        - `git tag "Implementacja" 68758f6 -a -m"Dodanie poważnej zawartości"`
    - pozwalają na późniejszy dostęp do commitów po nazwie zamiast numerze

--- 
- **gałęzie**
    - nowa gałąź zaczyna od danego momentu i stanu aktywnego repozytorium
    - git merge [nazwa]
        - łączy gałąź do aktywneej("checked out") gałęzi
    - git branch
        - lista gałęzi
        - git branch [nazwa]
            - tworzenie gałęzi
        - git branch -m [nazwa]
            - zmiana nazwy gałęzi
    - git checkout
        - zmiana aktywnej gałęzi
        - git checkout -b [nazwa]
            - utworzenie nowej gałęzi i przejście na nią
        - zmiana aktywnych gałęzi nie gubi zmian, jeżeli zostaną zacommitowane co pozwala zmieniać dowolnei gałęzie bez obawy przed utrata zmian
        - git checkout [numer_commit/nazwa_tag]
            - przejście do dowolnego starszego commita w gałęzi
    - tip
        - najnowszy commit w gałęzi
    - head
        - wskaźnik na najnowszy commit w gałęzi(tip)
        - '.git/refs/heads' przechowuje wskaźniki dla wszystkich lokalnych gałęzi
    - HEAD
        - aktualny aktywny commit odnoszący się do zawartości katalogu roboczego w danym momencie
        - pozwala na potwierdzenie aktualnego katalogu roboczego z konsoli
    - detached HEAD
        - wskazuje na starszy commit danej gałęzi i pozwala na dostęp do przestarzałego katalogu roboczego

---
- **repozytoria**
    - 