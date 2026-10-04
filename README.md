# ledgdex.github.io

This repository is the website of [ledgdex](https://github.com/ledgdex/ledgdex). GitHub Pages serves it at https://ledgdex.github.io.

The site has three parts. Each part is a dex from the ledgdex repository:

| Folder here | Pages | Source in ledgdex/ledgdex |
|---|---|---|
| the root | the home page, [Live Markets](https://ledgdex.github.io/livemarkets.html) and [About](https://ledgdex.github.io/about.html) | `home/` |
| `viewer/` | the [viewer](https://ledgdex.github.io/viewer/index.html) and its JavaScript modules | `viewer/` |
| `docs/` | the [docs](https://ledgdex.github.io/docs/), a ledgdex | `guide/dex/` |

The root file `viewer.html` sends old links to `viewer/index.html`. It keeps the query of the link.

Dexweb publishes all files here. Do not edit them by hand. To publish, use a clone of ledgdex/ledgdex:

```
cd home && python run.py               # the home pages, at the root
cd viewer && python run.py             # the viewer, in viewer/
cd guide/dex && ledgdex publish .      # the docs, in docs/
```

Dexweb never deletes files here. When a page does not exist any more, delete its file by hand.

The viewer keeps sealed keys in the storage of the browser. Each page on this origin can read that storage. GitHub Pages serves each repository of the ledgdex organization from this origin when Pages is on for that repository. So obey these rules:

- Turn on Pages only for this repository.
- Give push access to this repository to the smallest possible number of people.
- Do not add scripts to the home pages or the docs. Only the viewer runs scripts.
