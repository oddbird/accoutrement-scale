accoutrement-scale
==================

Sass typography [Accoutrement][accoutrement]
by [OddBird][oddbird].
Sass size & scale management tools.
Generate sizes based on [modular scales][ms],
gather all your sizes into a single map,
and access them by name in various ways.

[accoutrement]: http://oddbird.net/accoutrement/
[oddbird]: http://oddbird.net/
[ms]: http://www.modularscale.com/


Quick Start
-----------

```bash
npm install accoutrement-scale
```

Import the library:

```scss
@import 'path/to/accoutrement-scale/sass/scale'
```

Establish your palette of ratios and sizes,
along with the default units needed for output:

```scss
$default-units: 'rem';

$ratios: (
  'my-ratio': 1.25,
);

$sizes: (
  'root': 24px,
  'rhythm': 'root' ('fifth': 1),

  'h1': 'root' ('my-ratio': 3),
  'h2': 'root' ('my-ratio': 2),
  'h3': 'root' ('my-ratio': 1),

  'page': '8in',
);
```

Access your sizes from anywhere,
with helpers for setting font-sizes and line-heights:

```scss
h1 {
  @include font-size('h1');
  max-width: size('page');
}
```

We can only calculate integer steps along an exponential scale,
but if you want more power,
install [MathSass][mathsass],
and we'll let them do the hard math.

```scss
$sizes: (
  'complex': 'root' ('my-scale': 1.25),
);
```

[mathsass]: https://github.com/terkel/mathsass
