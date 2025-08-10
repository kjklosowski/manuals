# Uniwersytet Gdański - Kulturoznawstwo

## Informacje podstawowe
Style CSL dla Kulturoznawstwa Uniwersytetu Gdańskiego jako pierwsze polskie style w bazie Citation Style Language nadają się w pełni do wykorzystania w humanistyce współczesnej/cyfrowej.
Opracowane są na podstawie [standardów redakcyjnych kierunku](https://fil.ug.edu.pl/sites/fil.ug.edu.pl/files/_nodes/strona/71884/files/kult._prace_standardy_redakcyjne_2.pdf).

Przygotowane są przede wszystkim dla osób studenckich korzystających z menedżerów bibliografii i piszących w oparciu o standardy redakcyjne tego kierunku.
Mogą cytować dla gry wideo, strony internetowe, posty w mediach społecznościowych, muzykę, filmy, seriale i inne.

Mogą być one także zaczątkiem innych styli dla polskiej humanistyki współczesnej/cyfrowej.

## Wersje i zachowanie
[Wersja na przypis dolny](https://github.com/citation-style-language/styles/pull/7547) – do zastosowania typowego.

[Wersja na przypis wewnątrztekstowy](https://github.com/citation-style-language/styles/pull/7549) – dodatkowo.

Pod względem tworzenia bibliografii zachowują się one identycznie.
Przypisy wewnątrztekstowe przybierają formę ````(Nazwisko, rok: lokalizator)```` lub ````(tytuł krótki, rok: lokalizator)````, jeśli autora brak.
Przypisy dolne tworzone są na podstawie wymagań kierunkowych.

## Pobieranie i instrukcja
Style można wykorzystać w każdym menedżerze bibliografii wspierającym [Citation Style Language](https://citationstyles.org/).
Autor rekomenduje [Zotero](https://www.zotero.org/).

Ponieważ styl nadal oczekuje na publikację w oficjalnym repozytorium, dostępny jest do pobrania zewnętrznie:

[Pobierz](https://1drv.ms/f/c/e41af7a6dec2cedb/EvbSEt05lm5Nr-KWliHWT5QBXWEJ43RmVP_-PJ25ZVqrJA?e=u1yFWq)

Style należy zaimportować w ręcznie. Dla przykładu, w Zotero odbywa się to poprzez wejście w ````Settings -> Cite```` i kliknięcie guzika z +.

## Zgodność i edycja
Świat przypisów jest nieustandaryzowany, różnorodny, a czasem nawet sprzeczny w ramach jednej instytucji.
Celem autora było zachowanie możliwie największej zgodności. Z racji na czynnik ludzki jest to jednak niemożliwe do osiągnięcia w 100%.

W zdecydowanej większości przypadków style te będą odpowiednie do większości prac zaliczeniowych, a nawet dyplomowych.
Jeśli jednak kwestie problematyczne pojawią się, należy pamiętać, że większość z nich da się rozwiązać bardzo prostą i szybką edycją kodu tych styli.
Taka edycja, choć wymaga oczywiście czasu, jest o całe rzędy wielkości bardziej efektywna niż ciągłe modyfikowanie przypisów manualnie.

Do wszelkich modyfikacji autor poleca [Visual CSL Editor](https://editor.citationstyles.org/visualEditor/), który umożliwia edycję w sposób wizualny, minimalizując konieczność własnoręcznego pisania kodu.
Style wydane są licencji [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). <b>Kluczowe jest respektowanie postanowień tej licencji!</b>

## Uwagi
Poniższa lista zawiera elementy, które najczęściej mogą wymagać zmian – wraz z instrukcjami, jak tych zmian dokonać samodzielnie.

<b>Autor zachęca do dalszego rozwijania tej listy, jeżeli nowe kwestie zostaną zauważone.</b>

### 1. Cytowanie filmów
Styl nie używa skrótów ````reż.```` i ````prod.````, choć standardy redakcyjne tego wymagają – utrudniłoby to cytowanie filmów na YouTube, których autorzy raczej nie są reżyserami.

Jeśli potrzebujesz tych skrótów:
1. W sekcji ````Inline Citations````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names````,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names````.
2. W sekcji ````Bibliography````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names````,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names````.
3. <b>We wszystkich tych miejscach</b>:
   - Używając ````+````, dodaj zmienną ````Label````, przenieś ją na samą górę drzewa ````Names````, ````suffix```` ustaw na ```` ```` (spacja), a zmienną ````form```` ustaw na ````short```` lub ````long```` (są też inne możliwe konfiguracje).

Pamiętaj, aby w takim przypadku filmy na YouTube w menedżerze bibliografii określić jako zwykła strona internetowa, a nie film!
  
### 2. Cytowanie muzyki
Cytowanie muzyki jest trochę nieintuicyjne, co jest ograniczeniem samego CSL, a konkretniej: dostępnych zmiennych w typie rekordu bibliograficznego ````song````.

Jeśli chcesz zacytować piosenkę będącą częścią albumu i chcesz podać autorów całego albumu, to musisz w menedżerze bibliografii dodać zmienną ````composer````, bo to ona jest ustawiona przed tytułem albumu jako „autor” albumu.
Jest to kwestia czysto techniczna i nie wpływa na funkcjonowanie cytowań.

### 3. Uwagi dotycząca sortowania bibliografii
Style korzystają z podstawowej logiki sortowania – najpierw po nazwiskach autorów od A do Z, a gdy autorów nie ma, to po tytułach od A do Z.

Może to jednak nieść za sobą nieoczywiste konsekwencje:
1. Przy cytowaniu filmów:
   - Ponieważ zmienne ````reżyser```` i ````producent```` nie są tym samym, co zmienna ````autor````, a filmy są często dziełami zbiorowymi, wszystkie one są sortowane po <b>tytułach</b> na samym końcu bibliografii (dopiero po autorach):
      - Jest to jednak problematyczne przy cytowaniu filmów na YouTube, których autorzy są już raczej autorami. Jeśli chcesz, by filmy na YouTube były sortowane razem z autorami, w menedżerze bibliografii określ je jako zwykła strona internetowa, a nie film.

### 4. Łacińskie i polskie skróty
Domyślnie używane są <i>italizowane</i> skróty <b>łacińskie</b>.

Aby zmienić język:
1. W sekcji ````Advanced````:
   - Idź do ````Locale -> Terms````.
2. <b>Wprowadź pożądane wartości tekstowe we wszystkich polach</b> ````Term````.

Aby zmienić <i>italizowanie</i>:
1. W sekcji ````Inline Citations````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names -> Et-al````,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names -> Et-al````,
   - Idź do ````If first -> Else-if song -> If composer -> Names -> Et-al````,
   - Idź do ````Else-If ibid-with-locator -> ibid (term)````,
   - Idź do ````Else-If ibid -> ibid (term)````.
2. W sekcji ````Bibliography````:
   - Idź do ````Else-if motion_picture -> If director -> Names -> Et-al````,
   - Idź do ````Else-if motion_picture -> If producer -> Names -> Et-al````,
   - Idź do ````Else-if song -> If composer -> Names -> Et-al````.
3. W sekcji ````Macros````:
   - W makrach: ````author````, ````author-bibliography````, ````editor-translator````, ````editor-translator-bibliography```` idź do ````Names -> Et-al````,
   - W makrze ````title-short```` idź do ````op-cit (term)````.
4. <b>We wszystkich tych miejscach zaznacz lub odznacz</b> <i>````I````</i>.

### 5. Imiona i nazwiska
W standardach redakcyjnych imiona i nazwiska przyjmują formę ````I. Nazwisko```` w przypisach oraz ````Nazwisko Imię```` w bibliografii.

Aby zmienić to zachowanie, musisz zmienić wartość dwóch zmiennych w kilku miejscach:
1. W sekcji ````Inline Citations````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names -> Name````,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names -> Name````,
   - Idź do ````If first -> Else-if song -> If composer -> Names -> Name````.
2. W sekcji ````Bibliography````:
   - Idź do ````If first -> Else-if motion_picture -> If director -> Names -> Name````,
   - Idź do ````If first -> Else-if motion_picture -> If producer -> Names -> Name````,
   - Idź do ````If first -> Else-if song -> If composer -> Names -> Name````.
3. W sekcji ````Macros````:
   - W makrach: ````author````, ````author-bibliography````, ````editor-translator````, ````editor-translator-bibliography```` idź do ````Names -> Name````.
4. <b>We wszystkich tych miejscach znajdziesz dwie zmienne</b>:
   - Zmienna ````initialize```` odpowiada za skracanie imienia – ustaw na ````true```` lub ````false````,
   - Zmienna ````name-as-sort-order```` odpowiada za kolejność:
      - Imię i nazwisko: ````name-as-sort-order```` ustaw na ```` ```` (spacja), a ````sort-separator```` na ````, ```` (przecinek i spacja),
      - Nazwisko i imię: ````name-as-sort-order```` ustaw na ````all````, a ````sort-separator```` na ```` ```` (spacja).

### 6. Redaktorzy i tłumacze
Styl domyślnie stosuje formę ````red. I. Nazwisko, tłum. I. Nazwisko```` w przypisach oraz ````red. Nazwisko Imię, tłum. Nazwisko Imię```` w bibliografii.

Równie często spotykanym zapisem jest jednak ````I. Nazwisko (red.), I. Nazwisko (tłum.)```` itd.

Jeśli potrzebujesz tego zachowania:
1. W sekcji ````Macros````:
   - W makrach ````editor-translator````, ````editor-translator-bibliography```` idź do ````Names````.
2. <b>W obu tych miejscach wykonaj następujące czynności</b>:
   - Przesuń zmienną ````Label```` pod zmienną ````Name````,
   - W zmiennej ````Label```` ustaw ````prefix```` na ````(````, a ````suffix```` na ````) ```` (zamknąć nawias i spacja).

### 7. Lokalizatory (tylko wersja na przypisy wewnątrztekstowe)
Styl w wersji na przypisy wewnątrztekstowe domyślnie stosuje następującą formę:
- Jeśli lokalizator jest stroną lub ich zakresem, zastosowana zostanie forma domyślna: ````Nazwisko, rok: X````,
- Jeśli wybrano inny typ lokalizatora, np. rozdział, dodane zostanie także skrótowe określenie wybranego typu lokalizatora, np: ````Nazwisko, rok: rozdz. X````.

Może pojawić się potrzeba całego szeregu zmian, np. zmiany ````:```` na ````,````, dodanie skrótu ````s. ```` przed stronami lub usunięcie wszystkich skrótów danego typu lokalizatora (np. ````rozdz.````).

Aby zmienić ````:```` na ````,````:
1. W sekcji ````Inline Citations````:
   - Idź do ````If author -> Group````,
   - Idź do ````Else -> Group````.
2. <b>W obu tych miejscach wykonaj następujące czynności</b>:
   - Ustaw ````delimiter```` na ````, ```` (przecinek i spacja).

Aby zmienić zachowanie skrótów danego typu lokalizatora:
1. W sekcji ````Macros````:
   - W makrze ````locator```` idź do ````Group````.
2. <b>Jeśli chcesz całkowicie usunąć skróty danego typu lokalizatora</b>:
   - Usuń cały blok ````Conditional```` przyciskiem ````-````.
3. <b>Jeśli chcesz dodać skrót także do stron<b>:
   - Wysuń zmienną ````locator (label)```` z bloku ````Conditional```` i umieść ją nad zmianną ````locator (variable)````, a następnie usuń blok ````Conditional```` przyciskiem ````-````.
