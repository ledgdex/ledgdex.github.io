# ledgdex.github.io

The website of [ledgdex](https://github.com/ledgdex/ledgdex), served by GitHub Pages at https://ledgdex.github.io:

- the home page, the [viewer](https://ledgdex.github.io/viewer.html), [live markets](https://ledgdex.github.io/livemarkets.html) and about: the viewer dex, from `viewer/` in ledgdex/ledgdex;
- [the docs](https://ledgdex.github.io/docs/) in `docs/`: a ledgdex, from `guide/dex/` in ledgdex/ledgdex.

Everything here is published by dexweb; do not edit it by hand. To publish, from a clone of ledgdex/ledgdex:

```
cd viewer && python run.py              # the viewer, at the root
cd guide/dex && ledgdex publish .       # the docs, in docs/
```

dexweb never deletes files here: remove a page that no longer exists by hand.

The viewer keeps sealed keys in browser storage, which every page on this origin can read. Every repository in the
ledgdex organization with GitHub Pages turned on is served from this origin, so only this repository may have Pages,
and push access to it should stay with as few people as possible.
