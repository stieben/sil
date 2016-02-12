# Search with grep

_#unix_ _#bash_ _#grep_ _#search_ _#regex_

Use grep to find strings in files.
You can use regular expressions.

## Find a literal string inside a directory

`grep -rin "<string>" <directory>`

- `-r` is for recursive search.
- `-i` means case insensitive.
- `-n` outputs line numbers.

Note that you need to escape special characters inside your search string: `\.`.

## More information

- [ubuntuusers Wiki](https://wiki.ubuntuusers.de/grep/) (German)
- [Wikipedia](https://en.wikipedia.org/wiki/Grep)

## Tools

- [Searchmonkey](http://searchmonkey.embeddediq.com/) is a GUI alternative and available as a [Debian package](https://packages.debian.org/search?keywords=searchmonkey).
