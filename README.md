Campbell+AppVeyor
==========

[![Build status](https://ci.appveyor.com/api/projects/status/github/USGS-OWI/campbell-appveyor?branch=master)](https://ci.appveyor.com/project/USGS-OWI/campbell-appveyor/branch/master)

This is a solution for continuous integration for Campbell Datalogger programs on Windows, using [AppVeyor](http://appveyor.com) -- a CI testing service similar to [Travis-CI](http://travis-ci.org).
Under the hood, campbell-travisis used to perform the testing.


Usage
-----

1. Sign up to [AppVeyor](http://appveyor.com).
2. [Enable testing](https://ci.appveyor.com/projects/new) for your project.
3. Save a copy of [`sample.appveyor.yml`](/sample.appveyor.yml) as `appveyor.yml` to the root of your project.
4. (Optional) Adapt `appveyor.yml` to your needs according to the [documentation](http://www.appveyor.com/docs/appveyor-yml).
5. Add the following line to `.Rbuildignore` of your project:

    ```
    ^appveyor\.yml$
    ```
6. Be sure to supply a `.gitattributes` file that takes care of fixing CRLF conversion settings that are relevant on Windows.  [The one in this repo](/.gitattributes) can be used for starters.
7. Push to your repo to start building.
8. (Optional) Add a badge as described in the "Badges" section of [your project's](https://ci.appveyor.com/projects) "SETTINGS" to your `README.md`.
9. Enjoy!


Acknowledgements
----------------

This wouldn't have been as easy without [r-travis](https://github.com/craigcitro/r-travis) and the experience gained there. Thanks!


Other branches
--------------

[![Build status for expected failure](https://ci.appveyor.com/api/projects/status/github/krlmlr/r-appveyor?branch=master-fail)](https://ci.appveyor.com/project/krlmlr/r-appveyor/branch/master-fail) ([`master-fail` branch](https://github.com/krlmlr/r-appveyor/tree/master-fail), failure expected)

[![Build status for run without copying R](https://ci.appveyor.com/api/projects/status/github/krlmlr/r-appveyor?branch=master-nocopy)](https://ci.appveyor.com/project/krlmlr/r-appveyor/branch/master-nocopy) ([`master-nocopy` branch](https://github.com/krlmlr/r-appveyor/tree/master-nocopy), probably will fail until an [issue with R](https://bugs.r-project.org/bugzilla/show_bug.cgi?id=15942) is resolved)
