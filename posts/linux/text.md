# Working with text

_#unix_ _#bash_ _#sed_ _#search_ _#sort_ _#regex_ _#text_

## Search and replace with `sed`

You can use regular expressions with `sed` to find and replace strings in files.

### Example: Delete all empty lines

```bash
sed --in-place '/^$/d' input.txt # /d flag for deletion
```

### Example: Replace all `\n` occurrences with actual newlines

```bash
sed --in-place 's/\\n/\n/g' input.txt
```

## Sort with `sort`

This will sort all lines alphabetically:

```bash
sort input.txt > output.txt
```

## Sources

- [Fibrevillage: Ways to remove empty lines in a file on Linux](https://www.fibrevillage.com/scripting/619-ways-to-remove-empty-lines-in-a-file-on-linux)
- [Geek University: Sort lines of a text file](https://geek-university.com/linux/sort-lines-of-a-text-file/)
- [StackOverflow: How to replace the string “\n” with an actual newline (\n)](https://stackoverflow.com/a/13611446/2040520)
- [StackOverflow: sed with option -i and flag /d set](https://stackoverflow.com/a/27762846/2040520)
