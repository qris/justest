justest
=======

Stripped-down Javascript test framework from Google Closure.

Extracted just the parts of Google Closure necessary to run basic unit
tests, as requested by @birdsarah, and put them into a minimal
infrastructure with a sample .html file (runner.html) and test library
(tests.js).

Using justest
-------------

* run your tests by opening `runner.html` in a browser, and check that
  the example test passes.
* write your tests in `tests.js` using the [Closure Library
assertions](http://docs.closure-library.googlecode.com/git/closure_goog_testing_asserts.js.html).

Extending justest
-----------------

If you want to use any more files extracted from
[Closure Library](http://docs.closure-library.googlecode.com/git/index.html),
you can either:

* load them manually by adding `<script>` tags in `runner.html`, or
* use Closure's dependency mechanism, as explained in the
[Closure tutorial](https://developers.google.com/closure/library/docs/tutorial).

To use Closure's dependency mechanism, you need to tell `goog.base` where
to find the new classes. Drop the Closure source files and their dependencies 
into the `closure` directory, then run `make`.  This will invoke the
[calcdeps](https://developers.google.com/closure/library/docs/calcdeps)
script, which rebuilds the `calculated_deps.js` file.

That file is sourced by `runner.html` and used by `goog.require`. So you
should then be able to load any components that those files declare (with
`goog.provide` statements) by adding `goog.require` statements to your
`tests.js` file.
