# Search and replace with sed

_#unix_ _#bash_ _#sed_ _#search_ _#regex_

You can use regular expressions with sed to find and replace strings in files.

## Example

Replace all `\n` occurrences with actual newlines:

```bash
sed --in-place 's/\\n/\n/g' input.txt
```

## Source

- [StackOverflow](https://stackoverflow.com/a/13611446/2040520)
