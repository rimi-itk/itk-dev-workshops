# Markdown

* [The Markdown Guide]
* *Github Flavored Markdown* udpensles i [Github Flavored Markdown Spec]
  * Kom i gang: <https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax>

## Værktøjer

[The Markdown Guide]

Markdown er bare rå tekst

[The Markdown Guide]

* [Emacs](https://www.gnu.org/software/emacs/)
* [VSCodium](https://vscodium.com/)
* [PhpStorm](https://www.jetbrains.com/phpstorm/)
* GitHub, fx <https://gist.github.com/>

### WAWYSIWYG

* `gh markdown-preview`

### Kodestandarder og -tjek

``` shell name=coding-standards-markdown
docker run --rm --volume "$PWD:/md" peterdavehello/markdownlint markdownlint --ignore LICENSE.md '**/*.md' --fix
docker run --rm --volume "$PWD:/md" peterdavehello/markdownlint markdownlint --ignore LICENSE.md '**/*.md'
```

<details>
<summary>markdownlint-konfiguration</summary>

``` jsonc
// .markdownlint.jsonc
{
  "default": true,
  // https://github.com/DavidAnson/markdownlint/blob/main/doc/md013.md
  "line-length": {
    "line_length": 120,
    "code_blocks": false,
    "tables": false
  },
  // https://github.com/DavidAnson/markdownlint/blob/main/doc/md024.md
  "no-duplicate-heading": {
    "siblings_only": true
  },
  // https://github.com/DavidAnson/markdownlint/blob/main/doc/md033.md
  "no-inline-html": {
    "allowed_elements": [
      "code",
      "kbd",
      "
    ]
  }
}
```

</details>

### Test og dovenskab

Markdown code runner (<https://github.com/mikkelricky/markdown-code-runner>) kan køre kodestumper i Markdown-filer, fx

``` shell name=markdown-code-runner-example
markdown-code-runner run coding-standards-markdown --echo '👉 '
```

`gh itkdev changelog` (<https://github.com/rimi-itk/gh-itkdev>) kan hjælpe med at oprette og vedligeholde
[`CHANGELOG.md`](https://keepachangelog.com/en/1.1.0/#filename).

[GitHub Flavored Markdown Spec]: https://github.github.com/gfm/
[The Markdown Guide]: https://www.markdownguide.org/
