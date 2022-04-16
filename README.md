# Programmazione

In questa repository sono raccolti i file di appunti relativi alle lezioni del
corso di programmazione. I singoli file `.md` vengono successivamente importati
su [Notion](https://www.notion.so/) nella pagina di [programmazione](https://www.notion.so/sravioli/Programmazione-3d138708b64e4b14b13148e9a060841c), nella sezione
[Appunti](https://www.notion.so/sravioli/Programmazione-3d138708b64e4b14b13148e9a060841c#dc1d583844874e4083b71b4db8e53883).

## `.gitignore`

Dato l'utilizzo di [husky](https://github.com/typicode/husky), vengono ignorati da git la cartella `.husky` e
il file delle impostazioni di husky.

## `regex.txt`

Durante la stesura degli appunti utilizzo delle parole chiave per velocizzare la
scrittura degli appunti, queste vengono successivamente trovate e sostituita
utilizzando delle REgular EXpressions (regex). Utilizzo il motore regex di
Sublime Text 3, più informazioni sul regex flavor [qui](https://docs.sublimetext.io/guide/usage/search-and-replace.html#regular-expressions). Le parole chiave
sono le seguenti:

| Keyword                      | Replacement                                        |
| :--------------------------- | :------------------------------------------------- |
| `-v` / `-f`                  | <ins>VERO</ins> / <ins>FALSO</ins>                 |
| `--keyword(:)`               | **_KEYWORD(:)_**                                   |
| `--key-word(:)`              | **_KEY_WORD(:)_**                                  |
| `--input(:)` / `--output(:)` | <ins>**INPUT(:)**</ins> / <ins>**OUTPUT(:)**</ins> |
| `.alg`                       | algoritmo                                          |
| `{[ note ]}`                 | `null`                                             |

Nel file [`regex.txt`](regex.txt) sono presenti i regex per cercare le parole chiave e quelli per sostituirle.
