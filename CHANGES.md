0.7.1.7 (5 June 2014)
---------------------

  * Allow `lens-4.2`
  * Test with GHC 7.8

0.7.1.6 (21 March 2014)
-----------------------

  * Allow `lens-4.1`

0.7.1.5 (10 March 2014)
-----------------------

  * Fix bug that was causing options set in profile or in-file options
    header to be ignored when doing pandoc writing, which affected
    e.g. table of contents setting.

0.7.1.4 (3 February 2014)
-------------------------

  * (#11) Workaround allowing [ghci] blocks in .lhs files containing
    lines that start with #

0.7.1.3 (30 January 2014)
-------------------------

  * Allow lens-4.0

0.7.1.2 (27 January 2014)
-------------------------

  * Allow blaze-html-0.7

0.7.1.1 (17 January 2014)
-------------------------

  * Bug fix: no table of contents is now actually the default, as advertised

0.7.1 (14 January 2014)
-----------------------

  * Allow pandoc-citeproc-0.3
  * Add --toc option for putting a table of contents at the top of a post

0.7.0.2 (4 December 2013)
-------------------------

  * Allow pandoc-citeproc-0.2

0.7.0.1 (7 November 2013)
-------------------------

  * Allow lens-3.10

0.7 (2 November 2013)
---------------------

  * Add support for citations.

0.6.3.1 (10 October 2013)
-------------------------

  * Allow haxr-3000.10

0.6.3 (30 September 2013)
-------------------------

  * Update to build against pandoc-1.12.  Note that BlogLiterately no
    longer builds with pandoc < 1.12.

0.6.2 (29 August 2013)
----------------------

  * Enable input in reStructuredText format

0.6.1 (27 August 2013)
----------------------

  * Automatically include necessary preamble (e.g. `<script>` tags)
    for the math mode chosen (*e.g.* MathJax)
  * Wrap the results of `hscolour` in `pre` and `code` tags with
    classes, to conform more closely to the style used by
    `highlighting-kate`
  * Output an entire URL upon a successful post

0.6.0.2 (15 May 2013)
---------------------

  * bump upper bound to allow HaXml-1.24

0.6.0.1 (27 March 2013)
-----------------------

  * bump upper bound to allow lens-3.9

0.6: 10 March 2013
------------------

  * Add support for "profiles" with sets of common options

  * Add support for reading options from inline blocks tagged `[BLOpts]`

  * Add support for reading post titles using pandoc-supported title
    block format, `% Title`

  * Transforms are now of type StateT (BlogLiterately, Pandoc) IO (),
    to allow transforms to alter the options record as well as the
    document

  * Add `centerImagesXF` to standard transforms

  * Move a bunch of ad-hoc functionality into standard transforms

  * Add `--html-only` option

  * bump `pandoc` upper bound to < 1.12

0.5.4.1: 18 February 2013
-------------------------

  * bump `blaze-html` upper bound to < 0.7

0.5.4: 24 January 2013
----------------------

  * Require `pandoc` 1.10.

0.5.3: 19 November 2012
-----------------------

  * New `--math` option for selecting pandoc math writing mode

  * Run the pandoc parser in "smart" mode, which generates proper en-
    and em-dashes, quotation marks, etc.

  * More updates for GHC 7.6.1 compatibility

  * Using `highlighting-kate` to highlight non-Haskell code was already
    the default; make this more clear.

    The `--other-kate` option is no more; now there are two options

      `--kate`
      `--no-kate`

    with `--kate` the default.

0.5.2.1: 19 September 2012
--------------------------

  * bump `base` upper bound to <4.7

0.5.2: 20 August 2012
---------------------

  * improvement to behavior of `--upload-images` flag: cache uploaded
    image server URLs, even across multiple runs, to avoid uploading
    the same image multiple times

  * bump dep upper bounds:
    - `split` to < 0.3
    - `cmdargs` to < 0.11

0.5.1: 30 July 2012
-------------------

  * Escape `<` and `>` characters in `ghci` output

  * Supress vertical whitespace following `ghci` commands that produce
    no output

  * add `centerImagesXF` transform (disabled by default)

  * create bug tracker and add `Bug-reports:` field to `.cabal` file

  * re-export `Text.BlogLiterately.Run` from `Text.BlogLiterately`

  * improved documentation

  * fix output of `--version`

0.5: 7 July 2012
----------------

  * expose internals as a library, and create framework for adding
    custom transformations to the pipeline

  * image uploads

  * ability to specify expected outputs in ghci blocks

  * prompt for password if not provided

  * bump `HaXml` upper bound to allow 1.23.*

0.4: 2 July 2012
----------------

  * Add special support for wordpress.com's LaTeX format

  * Support for `[ghci]` blocks with contents automatically passed
    through `ghci` and results typeset

  * Support for tags

  * Support for creating "pages" as well as posts (WordPress only)

  * New standalone documentation

  * Code cleanup

  * Update to build with GHC 7.4.1
