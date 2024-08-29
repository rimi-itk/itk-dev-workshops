# itk-dev-workshops

## Coding standards

```shell name=coding-standards-markdown
docker run --rm --volume $PWD:/md peterdavehello/markdownlint markdownlint --ignore LICENSE.md '**/*.md' --fix
docker run --rm --volume $PWD:/md peterdavehello/markdownlint markdownlint --ignore LICENSE.md '**/*.md'
```
