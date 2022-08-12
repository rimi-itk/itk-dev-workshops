# Keyboard shortcuts

Using keyboard shortcuts is essential for working efficiently with a computer.

## Notation

<kbd>Ctrl-X</kbd> means press the <kbd>Ctrl</kbd> key and the <kbd>X</kbd> key
simultaneously (a “chord”). <kbd>Ctrl X</kbd> means press the <kbd>Ctrl</kbd>
key and then press the <kbd>X</kbd> (a “sequence”).

Windows users should substitute <kbd>Cmd</kbd> with <kbd>Ctrl</kbd>.

## Pro tips

* Use an American keyboard layout for programming[^1]
  * Some even map <kbd>1</kbd> to insert <kbd>!</kbd> and <kbd>Shift-1</kbd> to
    insert <kbd>1</kbd> because <kbd>!</kbd> is used more often than
    <kbd>1</kbd> in programming.
* Use the cAPS lOCK key as a Control key (<kbd>Ctrl</kbd>)[^1]
* Normalize shortcuts for similar actions in different applications, i.e. use
  <kbd>Cmd-'</kbd> and <kbd>Cmd-;</kbd> for “Step over (next function call)” and
  “Step into (next function call)”, respectively, when debugging in your editor
  *and* in your browser.
* Learn how to navigate (see [Navigation](#navigation))
* Learn how to create new shortcuts

## The classics

| Shortcut               | Description                             |
|------------------------|-----------------------------------------|
| <kbd>Cmd-C</kbd>       | Copy selected text to clipboard         |
| <kbd>Cmd-X</kbd>       | Cut selected text to clipboard          |
| <kbd>Cmd-V</kbd>       | Paste from clipboard                    |
| <kbd>Cmd-Shift-V</kbd> | Paste from clipboard without formatting |

## Navigation

Apart from section/paragraph and parenthesis stuff these will also work in your
terminal.

| Shortcut              | Description                                                                             |
|-----------------------|-----------------------------------------------------------------------------------------|
| <kbd>Ctrl-A</kbd>     | Go to start of line                                                                     |
| <kbd>Ctrl-E</kbd>     | Go to end of line                                                                       |
| <kbd>Ctrl-P</kbd>     | Alternative to <kbd>up</kbd>                                                            |
| <kbd>Ctrl-N</kbd>     | Alternative to <kbd>down</kbd>                                                          |
| <kbd>Ctrl-left</kbd>  | Go one word back                                                                        |
| <kbd>Ctrl-right</kbd> | Go one word forward                                                                     |
| <kbd>Ctrl-K</kbd>     | Delete to end of line                                                                   |
| <kbd>Ctrl-up</kbd>    | Section/paragraph up                                                                    |
| <kbd>Ctrl-down</kbd>  | Section/paragraph down                                                                  |
| <kbd>Ctrl-Cmd-N</kbd> | Go to matching parenthesis or Go to next parenthesized block (depending on context)     |
| <kbd>Ctrl-Cmd-P</kbd> | Go to matching parenthesis or Go to previous parenthesized block (depending on context) |

### Switching between applications

| Shortcut                 | Description          |
|--------------------------|----------------------|
| <kbd>Cmd-Tab</kbd>       | Next application     |
| <kbd>Cmd-Shift-Tab</kbd> | Previous application |

Pro tip: Use [Grid spaces](https://github.com/mikkelricky/grid-spaces) or
similar tools
(<https://discuss.binaryage.com/t/can-we-help-test-total-spaces-3-if-we-have-apple-silicon/8199/158>).

### Switching tabs

| Shortcut               | Description            |
|------------------------|------------------------|
| <kbd>Cmd-Ctrl-[</kbd>  | Previous tab           |
| <kbd>Cmd-Ctrl-]</kbd>  | Next tab               |
| <kbd>Cmd-Shift-[</kbd> | Move current tab left  |
| <kbd>Cmd-Shift-]</kbd> | Move current tab right |

### Windows

| Shortcut | Description     |
|----------|-----------------|
|          | Maximize window |

## Jira

| Shortcut     | Description  |
|--------------|--------------|
| <kbd>.</kdb> | Do something |

## Terminal (Command line)

| Shortcut       | Description                                   |
|----------------|-----------------------------------------------|
| <kbd>Tab</kbd> | Completion (use this often and strategically) |
| 👻             | Select text from terminal output              |

Pro tip: Make it possible to open urls in your default browser from the terminal
by clicking with the mouse (!), e.g. <kbd>Cmd-click</kbd>.
[Choosy](https://www.choosyosx.com/) is your friend.

## Selecting text

Hold down <kbd>Shift</kbd> while navigating.

## Browsers

| Shortcut         | Description       |
|------------------|-------------------|
| <kbd>Cmd-L</kbd> | Focus address bar |
| <kbd>Cmd-T</kbd> | Open new tab      |
| <kbd>Cmd-W</kbd> | Close current tab |

## PhpStorm

| Shortcut                                                | Description                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <kbd>Shift-F6</kbd>                                     | Refactor code                                                                                       |
| <kbd>Shift Shift</kbd>                                  | Go to File…                                                                                         |
| <kbd>Cmd-. Ctrl-S K E Y M A P</kbd>                     | Edit and create shortcuts                                                                           |
| <kbd>Cmd-. Ctrl-S L I V E Space T E M P L A T E S</kbd> | Edit and create [live templates](https://www.jetbrains.com/help/phpstorm/using-live-templates.html) |

### Example live template

`phpde`:

```php
header('content-type: text/plain'); echo var_export(null$END$, true); die(__FILE__.':'.__LINE__.':'.__METHOD__);
```

## Spreadsheets (Excel, Google Sheets)

| Shortcut      | Description                                                   |
|---------------|---------------------------------------------------------------|
| <kbd>F2</kbd> | Edit cell content                                             |
| <kbd>F4</kbd> | Cycle through absolute references (when editing cell content) |

* [Keyboard shortcuts in Excel (Windows)](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f#bkmk_frequent&PickTab=Windows)
* [Keyboard shortcuts in Excel (macOS)](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f#bkmk_frequent&PickTab=macOS)

## Emacs (mostly for fun)

If you don’t already know these, you don’t need them …

| Shortcut                                                | Description |
|---------------------------------------------------------|-------------|
| <kbd>Ctrl-X 8 ' e</kbd>                                 | Insert `é`  |
| <kbd>Ctrl-X 8 " u</kbd>                                 | Insert `ü`  |
| <kbd>Ctrl-X 8 Enter C H E C K Space M A R K Enter</kbd> | Insert `✓`  |

[^1]: Your rheumatologist will thank you!
