# To jest ***bardzo*** ważny tytuł!
## Zasługuje na szacunek.

## Procedury Git
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
- **tagi**
 - lightweight - skrót SHA-1 commita
 - annotated - dane autora, data, komentarz *i SHA-1* danego commita
 - git tag [nazwa] [numer_commit]
  - lightweight
  - `git tag "Wprowadzenie" 39f7004`
 - git tag [nazwa] [numer_commit] -a -m"[komentarz]"
  - annotated
  - `git tag "Implementacja" 68758f6 -a -m"Dodanie poważnej zawartości"`
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