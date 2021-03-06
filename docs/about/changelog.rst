.. _changelog:

*************
Change Log
*************

All notable changes to PySS3 will be documented here.

[0.4.0] 2020-02-11
==================

Among other minor improvements and changes, the most important ones that were added are:

Added
-----

- ``SS3`` class:
  - The classifier now explicitly supports multi-label classification:
    - Created the following two methods in ``SS3`` class: `classify_multilabel() <../api/index.html#pyss3.SS3.classify_multilabel>`__ and `classify_label() <../api/index.html#pyss3.SS3.classify_label>`__ (`0759bca <https://github.com/sergioburdisso/pyss3/commit/0759bca4392b2441d8a3668c8aca6bd85791e06f>`__).
    - A ``multilabel`` argument was added to the ``predict`` method (`c5ac946 <https://github.com/sergioburdisso/pyss3/commit/c5ac94681196fb5f7b22fe39a9f6b5bda5362d13>`__). 
  - A new `extract_insight() <../api/index.html#pyss3.SS3.extract_insight>`__  method was added to the ``SS3`` class. This method, given a document, returns the pieces of text that were involved in the classification decision (`eee1e29 <https://github.com/sergioburdisso/pyss3/commit/eee1e292f410679ea3d25ba45bc1e70c57a3613c>`__).
  - Created four new methods to allow the user to set the delimiters (`b632fe0 <https://github.com/sergioburdisso/pyss3/commit/b632fe05526ed7596b49867094a56718e6fbc219>`__): `set_block_delimiters() <../api/index.html#pyss3.SS3.set_block_delimiters>`__, `set_delimiter_paragraph <../api/index.html#pyss3.SS3.set_delimiter_paragraph>`__, `set_delimiter_sentence <../api/index.html#pyss3.SS3.set_delimiter_sentence>`__, and `set_delimiter_word <../api/index.html#pyss3.SS3.set_delimiter_word>`__.

- Live Test tool:

  - Improved the the interface by which "Live Test" Server was called from source code, now its usage is more user-friendly and less misleading (read `516b526 <https://github.com/sergioburdisso/pyss3/commit/516b52685da3649dfcb64650d3cdaf4ee5ae8d3a>`__ for more info).
  - Improved the way by which multi-label classification was carried out in the Web interface (`046f9f4 <https://github.com/sergioburdisso/pyss3/commit/046f9f424a241ce0cdef833d2561ff80bb3f5b2e>`__).

- Improved how PySS3 handles verbosity levels (read `216be41 <https://github.com/sergioburdisso/pyss3/commit/216be41e4824f60071be219ce783134528cde795>`__ for more info ): created the `set_verbosity() <../api/index.html#pyss3.set_verbosity>`__ function.


[0.3.9] 2019-11-27
==================

Added
-----
- Live Test: layout updated.
- PySS3 Command Line: ``frange`` function added as an alias of ``r`` for the ``grid_search`` command.

Fixed
-----
- PySS3 Command Line: live_test always lunch the server with no documents (even when before "live_test a/path")
- Live Test:sentences starting with "unknown" token were not included in the "Advanced" interactive chart

[0.3.8] 2019-11-25
==================

Fixed
-----
- Server: fixed bug that stopped the server when receiving arbitrary bytes (not utf-8 strings)
- PySS3 Command Line: fixed bug when loading live_test with a non existing path
- Live Test: now the user can select one-letter words (and are also included in the "advanced" live chart)


[0.3.7] 2019-11-22
==================

Added
-----
- Summary operators are not longer static.
- ``Server.set_testset_from_files`` lazy load.

Fixed
-----
- Evaluation plot: confusion matrices size when working with k-folds


[0.3.6] 2019-11-14
==================

Added
-----
- ``Dataset`` class added to ``pyss3.util`` as an interface to help the user to load/read datasets. Method ``Dataset.load_from_files`` added
- Documentations updated

[0.3.5] 2019-11-12
==================

Added
-----
- PySS3 Command Line Python 2 full compatibility support

Fixed
-----
- Matplotlib set_yaxis bug fixed


[0.3.4] 2019-11-12
==================

Fixed
-----
- Dependencies and compatibility with python 2 Improved


[0.3.3] 2019-11-12
==================

Fixed
-----
- Setup and tests fixed


[0.3.2] 2019-11-12
==================

Added
-----
- Summary operators: now it is possible to use user-defined summary operators, the following static methods were added to the ``SS3`` class: `summary_op_ngrams`, `summary_op_sentences`, and `summary_op_paragraphs`.


[0.3.1] 2019-11-11
==================

Added
-----
- update: some docstrings were improved
- update: the README.md / Pypi Description file.

Fixed
-----
- Python 2 and 3 compatibility problem with scikit-learn (using version 0.20.1 from now on)
- PyPi: setup.py: `long_description_content_type` set to `'text/markdown'`