Accoutrement-Scale Changelog
============================


3.1.0 - UNRELEASED
------------------
- Add math functions:
  `add`/`plus`, `minus`/`subtract`, `times`/`multiply`, and `divide` –
  for use in scale maps, e.g. `'new-size': 'size1' ('add': 'size2')`


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
