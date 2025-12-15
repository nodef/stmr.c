# stmr(3) [![Build Status][travis-badge]][travis] [![Coverage Status][coveralls-badge]][coveralls]

Martin Porter’s [Stemming algorithm][algo] as a C library, by [Titus](https://github.com/wooorm).
There’s also a CLI: [stmr(1)][cli].

## Installation

Run:
```bash
$ npm i stmr.c
```

And then include `stmr.h` as follows:
```c
#include "node_modules/stmr.c/stmr.h"
```

You may also want to include `stmr.c` as follows:
```c
#ifndef __STMR_C__
#define __STMR_C__
#include "node_modules/stmr.c/stmr.c"
#endif
```

This will include both the function declaration and their definitions into a single file.

<br>

Or use

[clib][]:

```bash
clib install wooorm/stmr.c
```

Or clone the repo.

## Usage

### `int stem(char *pointer, int start, int end)`

```c
#include <stdio.h>
#include <string.h>
#include "stmr.h"

int
main(int argc, char **argv) {
  char *word = argv[1];

  int end = stem(word, 0, strlen(word) - 1);

  word[end + 1] = 0;

  printf("%s", word);
}
```

## Related

*   [`stemmer`][lib] — Same algorithm in JavaScript
*   [`stmr`][cli]
    — CLI in C

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definitions -->

[travis-badge]: https://img.shields.io/travis/wooorm/stmr.c.svg

[travis]: https://travis-ci.org/wooorm/stmr.c

[coveralls-badge]: https://img.shields.io/coveralls/wooorm/stmr.c.svg

[coveralls]: https://coveralls.io/github/wooorm/stmr.c

[license]: license

[author]: http://wooorm.com

[algo]: http://tartarus.org/martin/PorterStemmer/

[cli]: https://github.com/wooorm/stmr

[lib]: https://github.com/words/stemmer

[clib]: https://github.com/clibs/clib

<br>
<br>


[![ORG](https://img.shields.io/badge/org-nodef-green?logo=Org)](https://nodef.github.io)
![](https://ga-beacon.deno.dev/G-RC63DPBH3P:SH3Eq-NoQ9mwgYeHWxu7cw/github.com/nodef/stmr.c)
[![SRC](https://img.shields.io/badge/src-repo-green?logo=Org)](https://github.com/wooorm/stmr.c)
