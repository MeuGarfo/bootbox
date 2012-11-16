# Bootbox - Twitter Bootstrap powered alert, confirm and flexible dialog boxes

Please see http://paynedigital.com/bootbox for full usage instructions, or head over to http://bootboxjs.com for
a demo page ([please feel free to improve it!](https://github.com/makeusabrew/bootbox/tree/gh-pages))

## Contact

The easiest thing is to [find me on twitter](http://twitter.com/makeusabrew): [@makeusabrew](http://twitter.com/makeusabrew)

## Submitting Pull Requests

* Please ensure that the test suite passes before submitting a PR
* If you've added new functionality, **please** include tests which validate its behaviour

## Running Tests

* Tests live in tests/test.*.js and are run using [Mocha](http://visionmedia.github.com/mocha/) - to run simply open tests/index.html in your browser.
* Alternatively, tests can be run headlessly using [mocha-phantomjs](http://metaskills.net/mocha-phantomjs/):
```
    phantomjs tests/vendor/mocha-phantomjs/lib/mocha-phantomjs.coffee tests/index.html
```

## A note on Bootstrap dependencies

Keeping track of issues has become increasingly difficult without a **strict**
dependency on specific minor versions of Bootstrap. The original intention was
that the 2.x.x series of Bootbox would simply require Bootstrap >= 2.x.x - since
both projects use Semantic Versioning this should have been possible. However,
Bootstrap 2.2.x (and possibly 2.1.x) introduced breaking changes - or changes
considered backward incompatible in the context of this project at least. Over
time bugs started getting raised which eventually turned out to be due to subtle
changes in Bootstrap's code. Therefore, **2.5.0** is the last release which will
support Bootstrap 2.0.x and is *not guaranteed* to work with anything higher than
Bootstrap 2.0.4.

### Roadmap

The next major release of Bootbox, 3.0.0, will address all the incompatible changes
introduced by Bootstrap 2.2.x. As such, Bootstrap 2.1.x is a bit of a wildcard and
will never be explicitly supported.

You can get a quick overview of the roadmap in the form of the project milestones
[as listed in the issue tracker](https://github.com/makeusabrew/bootbox/issues/milestones)

## Latest Release: 2.5.0

**This will be the last version of the library which supports Bootstrap 2.0.x**

* add option to specify proper href attributes for buttons instead of callbacks (@StevePotter)
* add option to override per-modal classes (@ciaranj)

### 2.4.2

* revert ```backdrop``` default value to 'static' instead of ```true``` to prevent background clicks dismissing dialogs (GH-55)

### 2.4.1

* fix ```backdrop``` when supplied as an argument to ```bootbox.dialog```
* fix incorrect README version

### 2.4.0

* add ```bootbox.backdrop(bool)``` method (@gucki)
* add default parameter option to ```bootbox.prompt``` (@pzgz)

### 2.3.3

* add inline ```overflow: hidden``` CSS property (GH-46)
* move license info to separate hosted file to reduce file size

### 2.3.2

* Change button href attributes to ```javascript:;``` (@joshnesbitt)
* Explicitly ```window.jQuery``` through to ```Bootbox``` object (@nuegon)


### 2.3.1

* Ensure bootbox.prompt() gives focus to input, disable input autocomplete

### 2.3.0

* Added bootbox.prompt() to mimic native prompt() method
* Added Russian locale (#27)

### 2.2.0

* Allowed button callbacks to explicitly return false to prevent dialog from closing (thanks @benoit-ponsero)
* Added version number to header comments (#26)

### 2.1.2

* Added close button to re-scoped click handler (thanks @SeanMcGee and @kentbrew)

### 2.1.1

* Fixed incorrect button click handler selector (thanks FGRibreau)

### 2.1.0

* Added support for Bootstrap's Glyphicons via the ```icon``` option
* Added inline license information into bootbox.js and bootbox.min.js
* Tidied up source a little

### 2.0.1

* Removed dummy Google Closure Compiler method from minified library (thanks j0k3r!)

### 2.0.0

* Updated Bootstrap dependency from 1.4 to 2.0
* Class definitions now require ```btn-``` prefix as per Bootstrap 2.0
* Added Brazilian locale
* Added ```animate``` dialog option
* Added ```bootbox.animate(bool)``` option to set default animation preference
* Animated dialogs now rely on ```bootstrap-transitions.js``` as required by Bootstrap 2.0

### 1.1.2

* Added licensing information to README

#### 1.1.1
* Updated german locale

#### 1.1.0
* Secondary option of two-button dialog no longer has 'danger' class
* New bootbox.modal() method for generic non-dialog popups
* Allow jQuery objects to be passed as main dialog argument

## License

(The MIT License)

Copyright (C) 2011-2012 by Nick Payne <nick@kurai.co.uk> 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE
