# Wikipedia / MediaWiki XML dump grepper

## Global installation: 
```bash
npm install dumpgrepper -g
dumpgrepper --help
bzcat dump.xml.bz2 | dumpgrepper <regexp>
```

## Local installation (from inside a git checkout)
```bash
npm install
node index --help
bzcat dump.xml.bz2 | node index <regexp>
```

## Options
- `-i`: Case-insensitive [default: false]
- `-m`: Treat ^ and $ as matching beginning/end of *each* line, instead of beginning/end of entire article. [default: false]
- `--color`: Highlight matched substring using color. Use --no-color to disable.  Default is "auto". [default: "auto"]
- `-l`:Suppress  normal  output;  instead  print the name of each article from which output would normally have been  printed. [default: false]

See the `dumpGrepPatterns/` folder for some example regexps.

## Getting wikipedia dumps
You can get dumps at [download.wikimedia.org](http://dumps.wikimedia.org/backup-index.html). You probably want the `pages-articles` dump, for example http://dumps.wikimedia.org/enwiki/20141106/enwiki-20141106-pages-articles.xml.bz2 (~10G).
