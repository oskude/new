# `new` : file templating system

`new` is a file templating system for the command line.

_It uses a template directory/file structure,_
```
❱ treecat ~/.local/share/new/templates/webapp
webapp/
  new.template
  │ §dir§:Dir
  │ §name§:Name
  │ §version§:Version
  ╰─────────────────────────────
  §dir§/
    manifest.webapp
    │ {
    │ 	"name": "§name§",
    │ 	"version": "§version§"
    │ }
    ╰────────────────────────
```

_asks user for values,_
```
❱ new webapp
Dir     : myapp
Name    : My App
Version : 0.0.1
```

_and replaces those in directory names, file names and content._
```
❱ treecat myapp
myapp/
  manifest.webapp
  │ {
  │ 	"name": "My App",
  │ 	"version": "0.0.1"
  │ }
  ╰────────────────────
```

> [`treecat`](https://github.com/oskude/treecat) is used here solely for presentation purposes.

## Documentation

  * TODO

## Dependencies

Tools that need to be installed in order to use `new`.

  * [Bash](http://www.gnu.org/software/bash/bash.html)
    for the core script
  * [Coreutils](http://www.gnu.org/software/coreutils/coreutils.html)
    for copying files and creating directories
  * [sed](http://www.gnu.org/software/sed/)
    for replacing text inside files

## Licence

Copyright © 2015 Andre Schmidt

This file is part of `new`.

`new` is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

`new` is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with Foobar.  If not, see <http://www.gnu.org/licenses/>.

