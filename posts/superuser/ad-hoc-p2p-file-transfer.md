# Ad hoc peer-to-peer file transfer

_#p2p_ _#file-sharing_

![xkcd #949: file transfer](../_img/xkcd-949-file_transfer.png)

Picture by [xkcd](https://xkcd.com/949/).

## Tools

There are various options to try.

### Inside the browser

- [Bitf.ly](https://bitf.ly/) (@[GitHub](https://github.com/bitfly-p2p/))
- [FilePizza](https://file.pizza/) (@[GitHub](https://github.com/kern/filepizza))
- [Instant.io](https://instant.io/) (@[GitHub](https://github.com/feross/instant.io))
- [MKStream](https://www.mkstream.club/) (@[GitHub](https://www.github.com/make-sity/mkstream))
- [ShareDrop](https://www.sharedrop.io/) (@[GitHub](https://github.com/cowbell/sharedrop))
- [xkcd949](http://xkcd949.com/)

### From the terminal

Check out [Magic Wormhole](https://github.com/warner/magic-wormhole).
Or, if you know what you do, try this:

```bash
cat $FILE | nc -l -p 80
```

This opens up a port to the internet and only works under certain circumstances.

## Credits

All ideas and projects collected from [Hacker News](https://news.ycombinator.com/item?id=11192398).
