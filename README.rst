====================================
Quality Assurance for Plone projects
====================================

Life, the Universe, and Everything
----------------------------------

Buildout configuration and tools for providing Quality Assurance for Plone projects.

Don't Panic
-----------

This repository contains a Buildout configuration to include Quality Assurance
tools in Plone projects.

The following tools are provided:

`createcoverage`_
    Single script to create test coverage reports.

`flake8`_
    A wrapper around `Pyflakes, pep8 and Ned Batchelder's McCabe script.

coverage.sh
    Single script to check if a minimum test coverage is assured (we could
    skip this if createcoverage could provide at some point this
    information directly).

rebuild_i18n.sh
    Single script to synchronize i18n pot files with all translatable strings
    extracted form the package scripts and templates. Will also report any
    errors and suspect untranslated messages found.

    If there is a variable 'package-languages' with the list of languages
    in the buildout section, this script will create automatically the initial
    structure of locales folder and files.

    Use something like this:

    [buildout]
    package-languages = es, pt_BR

`z3c.dependencychecker`_
    Checks which imports are done and compares them to what's in setup.py and
    warn when discovering missing or unneeded dependencies. This is becoming
    increasingly important with the arrive of Plone 4.3.

`zptlint`_
    Runs the `Zope Page Templates`_ parser and output errors.

Mostly Harmless
---------------

Got an idea? Found a bug? Let me know by `opening a support ticket`_.

.. _`createcoverage`: https://pypi.python.org/pypi/createcoverage
.. _`flake8`: https://pypi.python.org/pypi/flake8
.. _`pep8`: https://pypi.python.org/pypi/pep8
.. _`pyflakes`: https://pypi.python.org/pypi/pyflakes
.. _`z3c.dependencychecker`: https://pypi.python.org/pypi/z3c.dependencychecker
.. _`zptlint`: https://pypi.python.org/pypi/zptlint
.. _`Zope Page Templates`: https://pypi.python.org/pypi/zope.pagetemplate
.. _`opening a support ticket`: https://github.com/hvelarde/qa/issues
