=============
Changelog
=============

2.2.0 (2024-10-21)
--------------------------------------------------

- Drop support for Python 3.8. Use older version for pre-built wheels.
  Note that it may work on these older versions, we are just no longer supporting
  and testing these Python versions, as this is end of life

- Add support for Python 3.13

2.1.0 (2024-03-21)
--------------------------------------------------

- Drop support for Python 3.6 and 3.7. Use older version for pre-built wheels.
  Note that it may work on these older versions, we are just no longer supporting
  and testing these Python versions 

- Add support for Python 3.12


2.0.0 (2023-01-14)
--------------------------------------------------

- Drop support for Python 2
- Drop support for 32 bits OSes
- Re-organize code such that sources are under src/, utilities under etc/
  and tests are under tests/
- Use pytest for testing and streamline tests to use a more conventional Python approach
- Build more compatible Linux wheels using "ci-build-wheel"


1.4.4 (2022-02-20)
--------------------------------------------------

- Minor rebuild to ensure Windows wheel documentation is correct ReST.


1.4.3 (2022-02-20)
--------------------------------------------------

- Use cibuildwheel to tests and build wheels on many OSes (with GitHub actions)
- Update supported Python versions. We cannot support what we cannot test:
  - Drop official support for Python 2.7. 
    Older version still run on Python 2.7+
  - Ensure that we compile with Python 3.10 and plan for 3.11 
  - Set minimum supported version of Python to 3.6
  - Run tests in CI on 3.6, 3.7, 3.8, 3.9 and 3.10

1.4.2 (2021-03-27)
--------------------------------------------------

- Add method ``iter_long``, that performs the modified
  Aho-Corasick search procedure matching the longest
  words from set.

1.4.1 (2020-01-26)
--------------------------------------------------

- Add method ``iter_long``, that performs the modified
  Aho-Corasick search procedure matching the longest
  words from set.

1.4.0 (2019-01-14)
--------------------------------------------------

- Change internal trie representation thanks to that performance
  of common operation is 1.5 - 2.5 times faster. Details are
  presented in https://github.com/WojciechMula/pyahocorasick/pull/107
  Warning: this change breaks compatibility of pickle and ``save()``
  format, this won't be possible to load files created in the
  previous version.

1.3.0 (2018-12-20)
--------------------------------------------------

- Add alternative pickling mechanism ``save()``/``load``, which
  requires less memory than the standard pickle solution (issue #102)

1.2.0 (2018-12-13)
--------------------------------------------------

- Add methods ``remove_word()``/``pop()`` (issue #79)

1.1.13.1 (2018-12-11)
--------------------------------------------------

- Fix manifest file

1.1.13 (2018-12-11)
--------------------------------------------------

- Fix pickling of large automatons (issue #50);
  The fix wouldn't be possible without great help and
  patience of all people involved:

  * **Emil Stenström** (@EmilStenstrom)
  * **David Woakes** (@woakesd)
  * **@Dobatymo**
  * **Philippe Ombredanne** (@pombredanne)
    
  The fix wouldn't also be possible without **Daniel Lemire** (@lemire),
  who gave me access to decent machines and I was able to test fixes
  on large data.

1.1.12 (2018-12-03)
--------------------------------------------------

- Add support for tuples of ints to ``iter()`` (by **Frankie Robertson**)

1.1.11 (2018-12-02)
--------------------------------------------------

- Reworked pickling code
- Fix pickling crash (issue #68)
- Fix pickling memory leak (issue #62)
- Fix documentation (by **Philippe Ombredanne**)
- Fix several latent bugs and problems

1.1.10 (2018-10-25)
--------------------------------------------------

- Fix handling of unicode in Python 3 (by **Frankie Robertson**)

1.1.9 (2018-10-25)
--------------------------------------------------

- Fix documentation typos (by **Sylvain Zimmer**)
- Add ability to skip white spaces in the input strings (by **@gladtosee**; issue #84)

1.1.8 (2018-04-25)
--------------------------------------------------

- Fix memory leak (issue #81)
- Add link to Python implementation from Abusix (by **Frederik Petersen**)
- Fix unit tests (by **Renat Nasyrov**)

1.1.7 (2018-02-23)
--------------------------------------------------

- Minor documentation fixes (by **Edward Betts**)
- Some internal improvements

1.1.6 (2017-11-27)
--------------------------------------------------

- Fix PyPI building (by **Philippe Ombredanne**; issue #71)

1.1.5 (2017-11-22)
--------------------------------------------------

- Fix handling of UCS2-encoded string (issue #53)
- Fix pickling error
- Several minor fixes and corrections to documentation
  and infrastructure (thanks to: **Jan Fan**, **@blackelk**,
  **David Woakes** and **Xiaopeng Xu**)

1.1.4 (2016-08-08)
--------------------------------------------------

- Fix URL in documentation (by **Philippe Ombredanne**)

1.1.3 (2016-08-07)
--------------------------------------------------

- Rewrite documentation and fix PyPI presentation (by **Philippe Ombredanne**)

1.1.2 (2016-08-06)
--------------------------------------------------

- Rewrite documentation continued (by **Philippe Ombredanne**)

1.1.1 (2016-05-29)
--------------------------------------------------

- Rewrite documentation, setup readthedocs.io__ page (by **Philippe Ombredanne**)
- Make the module compilable in Windows using MSVC compiler (issue #11)
- Fix ``get()`` method that crashed when trie was empty (issue #22)
- Fix pickling problem (issue #26)
- Add ``__sizeof__()`` method (issue #25)

__ https://pyahocorasick.readthedocs.io/en/latest/

1.1.0 (2016-04-26)
--------------------------------------------------

- Support for Python 2 (with help from **Philippe Ombredanne**; issue #12)

1.0.3 (2016-04-24)
--------------------------------------------------

- Fix memory leak (by **Jonathan Grs**; issue #9)

1.0.2 (2016-04-23)
--------------------------------------------------

- Fix range parsing (by **Jonathan Grs**; issue #10)
- Fix pickling on 64-bit machines (issue #20)
- Update documentation regarding wildcards

1.0.1 (2016-04-19)
--------------------------------------------------

- Fix Unicode handling during automaton build (issue #8)
- Fix some 64-bit code issues (issue #5)
- Fix documentation (thanks to **Pastafarianist**)

1.0.0 (2014-11-25)
--------------------------------------------------

- The first version available through PyPi
