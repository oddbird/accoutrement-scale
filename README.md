accoutrement-scale
==================

Sass size & scale management tools
by [OddBird][oddbird],
part of our [Accoutrement][accoutrement] suite.
Gather all your sizes into a single map,
generate new sizes based on [modular scales][ms]
or arbitrary functions,
and access them by name.

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

Establish your palette of ratios and sizes:

```scss
$ratios: (
  'my-ratio': 1.25,
);

$sizes: (
  'root': 24px,
  'rhythm': 'root' ('fifth': 1, 'convert-units': 'rem'),

  'h1': 'root' ('my-ratio': 3),
  'h2': 'root' ('my-ratio': 2),
  'h3': 'root' ('my-ratio': 1),

  'page': '8in',
);
```

Results will be returned in the units they were defined,
but can be converted in the map settings (as above),
or on-the-fly using `size`:

```scss
.example {
  // size('page') would return `8in`...
  width: size('page', 'px');
}
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
