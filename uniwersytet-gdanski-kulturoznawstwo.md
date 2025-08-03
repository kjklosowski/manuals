## Uniwersytet Gdański - Kulturoznawstwo

### Informacje podstawowe
Style CSL dla Kulturoznawstwa Uniwersytetu Gdańskiego jako pierwsze polskie style w bazie Citation Style Language nadają się w pełni do wykorzystania w humanistyce współczesnej/cyfrowej.
Opracowane są na podstawie [standardów redakcyjnych kierunku](https://fil.ug.edu.pl/sites/fil.ug.edu.pl/files/_nodes/strona/71884/files/kult._prace_standardy_redakcyjne_2.pdf).
Przygotowane są przede wszystkim dla osób studenckich korzystających z menedżerów bibliografii i piszących w oparciu o standardy redakcyjne tego kierunku.
Mogą cytować dla gry wideo, strony internetowe, posty w mediach społecznościowych, muzykę, filmy, seriale i inne.
Mogą być one także zaczątkiem innych styli dla polskiej humanistyki współczesnej/cyfrowej.

### Wersje i zachowanie
[Wersja na przypis dolny](https://github.com/citation-style-language/styles/pull/7547) – do zastosowania typowego.

[Wersja na przypis wewnątrztekstowy](https://github.com/citation-style-language/styles/pull/7549) – dodatkowo.

Pod względem tworzenia bibliografii zachowują się one identycznie.
Przypisy wewnątrztekstowe przybierają formę ````(autor, rok: lokalizator)```` lub ````(tytuł krótki, rok: lokalizator)````, jeśli autora brak.
Przypisy dolne tworzone są na podstawie wymagań kierunkowych.

### Pobieranie i instrukcja
Style można wykorzystać w każdym menedżerze bibliografii wspierającym [Citation Style Language](https://citationstyles.org/).
Autor rekomenduje [Zotero](https://www.zotero.org/).

Ponieważ styl nadal oczekuje na publikację w oficjalnym repozytorium, dostępny jest do pobrania zewnętrznie:

[Pobierz](https://1drv.ms/f/c/e41af7a6dec2cedb/EvbSEt05lm5Nr-KWliHWT5QBXWEJ43RmVP_-PJ25ZVqrJA?e=u1yFWq)

Style należy zaimportować w ręcznie. Dla przykładu, w Zotero odbywa się to poprzez wejście w ````Settings -> Cite```` i kliknięcie guzika z +.

### Zgodność i edycja
Świat przypisów jest nieustandaryzowany, różnorodny, a czasem nawet sprzeczny w ramach jednej instytucji.
Celem autora było zachowanie możliwie największej zgodności. Z racji na czynnik ludzki jest to jednak niemożliwe do osiągnięcia w 100%.

W zdecydowanej większości przypadków style te będą odpowiednie do większości prac zaliczeniowych, a nawet dyplomowych.
Jeśli jednak kwestie problematyczne pojawią się, należy pamiętać, że większość z nich da się rozwiązać bardzo prostą i szybką edycją kodu tych styli.
Taka edycja, choć wymaga oczywiście czasu, jest o całe rzędy wielkości bardziej efektywna niż ciągłe modyfikowanie przypisów manualnie.

Do wszelkich modyfikacji autor poleca [Visual CSL Editor](https://editor.citationstyles.org/visualEditor/), który umożliwia edycję w sposób wizualny, minimalizując konieczność własnoręcznego pisania kodu.
Style wydane są licencji [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). <b>Kluczowe jest respektowanie postanowień tej licencji!</b>

Poniższa lista zawiera elementy, które najczęściej mogą wymagać zmian – wraz z instrukcjami, jak tych zmian dokonać samodzielnie.

<b>Autor zachęca do dalszego rozwijania tej listy, jeżeli nowe kwestie zostaną zauważone.</b>
### Uwagi
#### 1. Łacińskie, a polskie skróty
Domyślnie używane są <i>italizowane</i> skróty <b>łacińskie</b>.

Aby to zmienić, w sekcji ````Advanced```` idź do ````Locale -> Terms```` i wprowadź pożądane wartości tekstowe we wszystkich polach ````Term````.

Opcje odpowiadające za <i>italizowanie</i> są rozsiane w kilku miejscach – należy zmienić je wszystkie:

1. W sekcji ````Inline Citations````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````If first -> Else-if song -> If composer -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````Else-If ibid-with-locator -> ibid (term)```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````Else-If ibid -> ibid (term)```` i zaznacz/odznacz <i>````I````</i>.
2. W sekcji ````Bibliography````:
   - Idź do ````Else-if motion_picture -> If director -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````Else-if motion_picture -> If producer -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - Idź do ````Else-if song -> If composer -> Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>.
3. W sekcji ````Macros````:
   - W makrach: ````author````, ````author-bibliography````, ````editor-translator````, ````editor-translator-bibliography```` idź do ````Names -> Et-al```` i zaznacz/odznacz <i>````I````</i>,
   - W makrze ````title-short```` idź do ````op-cit (term)```` i zaznacz/odznacz <i>````I````</i>.
