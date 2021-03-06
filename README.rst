Overview
========

:deployment:
    .. image:: https://img.shields.io/pypi/v/persontitles
        :alt: PyPI

    .. image:: https://img.shields.io/pypi/pyversions/persontitles
        :alt: PyPI - Python Version

:test/coverage:
    .. image:: https://app.codacy.com/project/badge/Grade/4bb124e2a8334d608c6a4d1cf1d1e543
        :target: https://www.codacy.com/gh/0LL13/persontitles/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=0LL13/persontitles&amp;utm_campaign=Badge_Grade

    .. image:: https://codecov.io/gh/0LL13/persontitles/branch/main/graph/badge.svg?token=G7O54JQHFE
        :target: https://codecov.io/gh/0LL13/persontitles

:build status:
    .. image:: https://img.shields.io/travis/0LL13/persontitles
        :alt: Travis (.org)

:docs:
    .. image:: https://img.shields.io/github/license/0LL13/persontitles
        :target: https://opensource.org/licenses/MIT


Dicts with lists containing academic degrees from the US, UK, and Germany,
peer titles from various countries (mixed), English and German job titles
(mixed) and German government jobs (male and female variants).

Features
--------

Check if a degree is a valid degree of chosen country.
Check if a degree is written correctly.
Check the number of US, UK, and German academic degrees.
Check if a title is a valid peer title of chosen country.
Check if a title is a job title.
Check if a title is a German government job (includes male and female variants).
Check if a word is a valid salutation.

Usage with degrees
------------------
::

    >>>from persontitles import academic_degrees
    >>>DEGREES = academic_degrees.degrees()

    >>>"Dr. iur. et rer. pol." in DEGREES["D"]
    >>>True

    >>>"bogus degree" in DEGREES["D"]
    >>>False

    >>>len(DEGREES["D"])
    >>>496

    >>>"MOcean" in DEGREES["UK"]
    >>>True

    >>>"Dr. iur." in DEGREES["UK"]
    >>>False

    >>>len(DEGREES["UK"])
    >>>404

    >>>"B.App.Sc(IT)" in DEGREES["US"]
    >>>True

    >>>len(DEGREES["US"])
    >>>614

Usage with titles
-----------------
::

    >>>from persontitles import peertitles
    >>>TITLES = peertitles.peertitles()

    >>>"Pfalzgräfin" in TITLES["German"]
    >>>True

    >>>"Archduke" in TITLES["English"]
    >>>True


Usage with job titles
---------------------
::

    >>>from persontitles import job_titles
    >>>JOB_TITLES = job_titles.job_titles

    >>>"CEO" in JOB_TITLES
    >>>True

    >>>"Facharzt Anästhesiologie" in JOB_TITLES
    >>>True

    >>>len(JOB_TITLES)
    >>>1023


Usage with German government jobs
---------------------------------
::

    >>>from persontitles import gov_jobs
    >>>GOV_JOBS = gov_jobs.gov_jobs()

    >>>"Amtsrat" in GOV_JOBS
    >>>True

    >>>"Amtsrätin" in GOV_JOBS
    >>>True

    >>>"Zweiter Konrektor" in GOV_JOBS
    >>>True

    >>>"Zweite Konrektorin" in GOV_JOBS
    >>>True

    >>>len(GOV_JOBS)
    >>>402


Usage with salutations
----------------------
::

    >>>from persontitles import salutations
    >>>SALUT = salutations.salutations()

    >>>"Mr." in SALUT
    >>>True

    >>>print(SALUT)
    >>>['Herr', 'Hr.', 'Frau', 'Fr.', 'Frl.', 'Mr.', 'Mr', 'Mrs.', 'Mrs', 'Ms.', 'Ms', 'Miss', 'Monsieur',
        'monsieur', 'Madame', 'madame', 'Señor', 'señor', 'Señora', 'señora']


Credits
-------

Credits to all the unsung heroes who maintain and update the Wikipedia.

Installation
------------
::

    pip install persontitles

or

::

    pipenv install persontitles

Contribute
----------

| **The best way to contribute is to update a wiki page with degrees or titles.**
| If you update the wiki pages and rebuild a new collection, the added degrees will
| be included (tested by myself).

Support
-------


Planned
-------

Add degrees in French or Spanish.
Add job roles, offices, job abbreviations, religious titles.


Warranty
--------

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, TITLE AND NON-INFRINGEMENT. IN NO EVENT SHALL
THE COPYRIGHT HOLDERS OR ANYONE DISTRIBUTING THE SOFTWARE BE LIABLE FOR ANY
DAMAGES OR OTHER LIABILITY, WHETHER IN CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.

In this particular package this means especially that there is no warranty
concerning the completeness of degrees for a country, the proper spelling of
the degrees listed, and the correctness of those degrees.

License
-------

MIT License

Copyright (c) 2020 Oliver Stapel
