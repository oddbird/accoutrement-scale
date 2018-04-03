Contributing to Accoutrement
============================

Bug reports and feature requests are welcome,
but code is even better!

In all cases,
we ask you to follow the
[Sass community guidelines](http://sass-lang.com/community-guidelines).


Development
-----------

Set up your environment
with the appropriate development dependencies:

```
yarn
```

As you work...

- Add or update any appropriate unit tests
  in the `test` directory,
  and make sure all tests are passing with `npm test`
- Add your changes to the [changelog](CHANGELOG.md)
- Update or add inline documentation
  using [SassDoc][sassdoc] as appropriate,
  and compile the docs with `gulp sassdoc`

[sassdoc]: http://sassdoc.com/


Committing
----------

Linting, testing, and documentation
should be done before every commit:

```
npm run commit
```

They can also be triggered individually:

```
# lint
gulp sasslint

# test with mocha/true, and compile ag-test CSS
npm test

# compile docs
gulp sassdoc
```

Optionally use `npm run test-libsass` for js-only tests,
or `rake test` for ruby-only environments.

Once you've fixed any final errors or typos,
commit your changes, and submit a pull request!


Pull Requests
-------------

We use the `master` branch for production-ready code,
and side-branches for everything in-progress
or up-for-debate.

When submitting a patch via pull request:

- Write a clear, descriptive commit message
- Keep it simple: one bug fix or feature per pull request
