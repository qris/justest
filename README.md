justest
=======

Stripped-down Javascript test framework from Google Closure.

Extracted just the parts of Google Closure necessary to run basic unit
tests, as requested by @birdsarah, and put them into a minimal
infrastructure with a sample .html file (runner.html) and test library
(tests.js).

To use:

* run your tests by opening `runner.html` in a browser.
* write your tests in `tests.js` using the [Closure Library
assertions](http://docs.closure-library.googlecode.com/git/closure_goog_testing_asserts.js.html).

If you want to use any more files extracted from
[Closure Library](http://docs.closure-library.googlecode.com/git/index.html),
you can drop them into the `closure` directory and run `make` to rebuild the
`calculated_deps.js` file. Then you should be able to load them by adding
`goog.require` statements to your `tests.js` file.
