Accoutrement-Scale Changelog
============================


5.0.0 - 09/13/17
----------------
- BREAKING: `$from-context` defaults to 'root' when available
- BUGFIX: Browser-em math requires `$from-context`
- NEW: Allow `size()` function to accept additional arguments
  (e.g. `$from-context` and `$to-context`) for unit-conversion.


4.0.2 - 09/13/17
----------------
- Recompile styleguide documentation.


4.0.1 - 09/13/17
----------------
- Publish missing styleguide documentation.


4.0.0 - 09/12/17
----------------

*Same as 4.0.0-alpha-1 - 09/06/17*

- BREAKING: Remove overly-opinionated baseline type tools
  including `font-size` and `baseline` mixins.
  These settings are more clear when established explicitly in CSS
- BREAKING: Rename `scale()` => `ratio()` to avoid conflicts with CSS
- BREAKING: Remove stand-alone `browser-ems()` function…
- NEW: Allow `browser-ems` as a `$to-unit` argument
  in the `contert-units()` function.
- NEW: Add (private) `pow()` functions,
  so that MathSass is no longer a dependency for non-integer steps


3.2.0 - 08/23/17
----------------
- NEW: Rename private `_get-ratio()` to public `scale()`
  for consistent access to ratios with map-key references.


3.1.1 - 05/27/17
----------------
- BUGFIX: Resolve problems with referencing `calc()` values


3.1.0 - 05/20/17
----------------
- Allow `calc()` values in scale maps
- Add `calc(%s + %s) ('root', 'rhythm')` syntax
  for building custom calc functions based on other map values
- Support single-argument adjustment functions
  by passing `null` to the arglist,
  e.g. `'size-name': 10rem / 3 ('round': null)`
- Include basic math functions:
  `add`/`plus`, `minus`/`subtract`, `times`/`multiply`, and `divide` –
  for use in scale maps, e.g. `'new-size': 'size1' ('add': 'size2')`
- Fix `safe-get-function` to expect first-class functions
  from external sources, and get local ones


3.0.0 - 03/08/17
----------------
- BREAKING: Don't convert units unless specifically requested.
  This allows you to define preferred units per-item
  in the configuration map.
- BREAKING: Remove `$default-units` setting. See above.
- Allow arbitrary adjustment functions
  in the `$sizes` map,
  e.g. `'my-size': 24px ('add': 12px)`,
  where `add` is an available function
  that will accept `24px, 12px` as arguments.
- Support first-class functions in Sass 3.5.
