# Tastaturgenveje

Tastaturveje er afgørende for effektiv brug af en datamat.

## Notation

<kbd>Ctrl-X</kbd> betyder tryk på <kbd>Ctrl</kbd>-tasten og <kbd>X</kbd>-tasten
på samme tid (a “akkord”). <kbd>Ctrl X</kbd> betyder tryk på
<kbd>Ctrl</kbd>-tasten og tryk derefter på <kbd>X</kbd> (en “sekvens”).

Windows-brugere skal skifte til Mac eller erstatte <kbd>Cmd</kbd> med
<kbd>Ctrl</kbd> i det følgende.

## Eksperttips

* Brug et amerikansk tastaturlayout til programmering[^1]
  * Nogle har endda en opsætning hvor <kbd>1</kbd> indsætter <code>!</code> og
    <kbd>Shift-1</kbd> indsætter <code>1</code> fordi <code>!</code> bruges
    oftere end <code>1</code> i programmering.
* Brug cAPS lOCK-tasten som en Control-tast (<kbd>Ctrl</kbd>)[^1]
* Brug de samme genveje for lignende handlinger i forskellige programmer, brug
  fx <kbd>Cmd-'</kbd> and <kbd>Cmd-;</kbd> til “Step over (next function call)”
  hhv. “Step into (next function call)” til debugging i din teksteditor *og* i
  din browser.
* Lær hvordan man bevæger sig rundt (se [Navigation](#navigation))
* Lær hvordan man laver nye tastaturgenveje

## Klassikerne

| Genvej                 | Beskrivelse                                  |
|------------------------|----------------------------------------------|
| <kbd>Cmd-C</kbd>       | Kopier valgt tekst til udklipsholderen       |
| <kbd>Cmd-X</kbd>       | Klip valgt tekst til udklipsholderen         |
| <kbd>Cmd-V</kbd>       | Indsæt fra udklipsholderen                   |
| <kbd>Cmd-Shift-V</kbd> | Indsæt fra udklipsholderen uden formattering |

## Mac (med amerikansk tastaturlayout)

| Genvej                 | Beskrivelse           |
|------------------------|-----------------------|
| <kbd>Cmd-’</kbd>       | Indsæt <code>æ</code> |
| <kbd>Cmd-O</kbd>       | Indsæt <code>ø</code> |
| <kbd>Cmd-A</kbd>       | Indsæt <code>å</code> |
| <kbd>Cmd-Shift-’</kbd> | Indsæt <code>Æ</code> |
| <kbd>Cmd-Shift-O</kbd> | Indsæt <code>Ø</code> |
| <kbd>Cmd-Shift-A</kbd> | Indsæt <code>Å</code> |

## Navigation

Bortset fra afsnits- og parentesstadset vil disse også virke i terminalen.
terminal.

| Genvej                | Beskrivelse                                                                                 |
|-----------------------|---------------------------------------------------------------------------------------------|
| <kbd>Ctrl-A</kbd>     | Gå til starten af linjen                                                                    |
| <kbd>Ctrl-E</kbd>     | Gå til slutningen af linken                                                                 |
| <kbd>Ctrl-P</kbd>     | Alternativ til <kbd>up</kbd>                                                                |
| <kbd>Ctrl-N</kbd>     | Alternativ til <kbd>down</kbd>                                                              |
| <kbd>Ctrl-left</kbd>  | Gå et ord tilbage                                                                           |
| <kbd>Ctrl-right</kbd> | Gå et ord frem                                                                              |
| <kbd>Ctrl-K</kbd>     | Slet til slutningen af linjen                                                               |
| <kbd>Ctrl-up</kbd>    | Gå et Afsnit up                                                                             |
| <kbd>Ctrl-down</kbd>  | Gå et afsnit ned                                                                            |
| <kbd>Ctrl-Cmd-N</kbd> | Gå til den matchende parentes eller Gå til næste parenteserede blok (afhængig af kontext)   |
| <kbd>Ctrl-Cmd-P</kbd> | Gå til den matchende parentes eller Gå til forrige parenteserede blok (afhængig af kontext) |

### Skift mellem programmer

| Genvej                   | Beskrivelse     |
|--------------------------|-----------------|
| <kbd>Cmd-Tab</kbd>       | Næste program   |
| <kbd>Cmd-Shift-Tab</kbd> | Forrige program |

Eksperttip: Brug [Grid spaces](https://github.com/mikkelricky/grid-spaces) eller lignende værktøjer
(<https://discuss.binaryage.com/t/can-we-help-test-total-spaces-3-if-we-have-apple-silicon/8199/158>).

### Skift mellem faner

| Genvej                 | Beskrivelse                     |
|------------------------|---------------------------------|
| <kbd>Cmd-Ctrl-]</kbd>  | Næste fane                      |
| <kbd>Cmd-Ctrl-[</kbd>  | Forrige fane                    |
| <kbd>Cmd-Shift-[</kbd> | Flyt nuværende fane til venstre |
| <kbd>Cmd-Shift-]</kbd> | Flyt nuværende fane til højre   |

### Windows

| Genvej | Beskrivelse     |
|--------|-----------------|
|        | Maximize window |

## Jira

| Genvej       | Beskrivelse        |
|--------------|--------------------|
| <kbd>.</kdb> | Gør et eller andet |

## Terminal (kommandolinje)

| Genvej         | Beskrivelse                                |
|----------------|--------------------------------------------|
| <kbd>Tab</kbd> | Fuldførelse (brug denne tit og strategisk) |
| 👻             | Vælg tekst fra terminaloutput              |

Eksperttip: Gør det muligt at åbne urler i din standardbrowser fra terminalen
med et museklik (!), fx <kbd>Cmd-click</kbd>.
[Choosy](https://www.choosyosx.com/) er din ven.

## Valg af tekst

Hold <kbd>Shift</kbd> ned mens du bevæger dig rundt med tastaturet.

## Browsere

| Genvej           | Beskrivelse           |
|------------------|-----------------------|
| <kbd>Cmd-L</kbd> | Aktiver adresselinjen |
| <kbd>Cmd-T</kbd> | Åbn ny fane           |
| <kbd>Cmd-W</kbd> | Luk nuværende fane    |

## PhpStorm

| Genvej                                                  | Beskrivelse                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <kbd>Shift-F6</kbd>                                     | Refactor code                                                                                       |
| <kbd>Shift Shift</kbd>                                  | Go to File…                                                                                         |
| <kbd>Cmd-. Ctrl-S K E Y M A P</kbd>                     | Edit and create shortcuts                                                                           |
| <kbd>Cmd-. Ctrl-S L I V E Space T E M P L A T E S</kbd> | Edit and create [live templates](https://www.jetbrains.com/help/phpstorm/using-live-templates.html) |

### Eksempel på “live template”

`phpde`:

```php
header('content-type: text/plain'); echo var_export(null$END$, true); die(__FILE__.':'.__LINE__.':'.__METHOD__);
```

## Regneark (Excel, Google Sheets)

| Genvej        | Beskrivelse                                                         |
|---------------|---------------------------------------------------------------------|
| <kbd>F2</kbd> | Rediger celleindhold                                                |
| <kbd>F4</kbd> | Cykl gennem absolutte referencer (under redigering af celleindhold) |

* [Tastaturgenveje i Excel (Windows)](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f#bkmk_frequent&PickTab=Windows)
* [Tastaturgenveje i Excel (macOS)](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f#bkmk_frequent&PickTab=macOS)

## Emacs (mest for sjov)

Hvis du ikke allerede kender disse så har du ikke brug for dem …

| Genvej                                                  | Beskrivelse |
|---------------------------------------------------------|-------------|
| <kbd>Ctrl-X 8 ' e</kbd>                                 | Indsæt `é`  |
| <kbd>Ctrl-X 8 " u</kbd>                                 | Indsæt `ü`  |
| <kbd>Ctrl-X 8 Enter C H E C K Space M A R K Enter</kbd> | Indsæt `✓`  |

[^1]: Din gigtlæge vil takke dig!
