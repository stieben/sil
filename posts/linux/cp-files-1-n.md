# Copy files: One to many

_#unix_ _#bash_

```bash
for file in file2 file3 ; do cp file1 "$file" ; done
for file in folder/* ; do cp example.txt "$file" ; done
```

## Source

- [StackOverflow: Linux commands to copy one file to many files](https://stackoverflow.com/a/9550556/2040520)
