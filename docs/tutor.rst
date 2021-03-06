.. _tutor:

Tutor development
=================

Start by cloning the Tutor repository::

    git clone https://github.com/regisb/tutor.git
    cd tutor/

Install requirements
--------------------

::

    pip install -r requirements/dev.txt

Run tests
---------

::

    make test

Yes, there are very few tests for now, but this is probably going to change.

Bundle ``tutor`` executable
---------------------------

::

    make bundle

Generate the documentation
--------------------------

::

    pip install sphinx sphinx_rtd_theme
    cd docs/
    make html

You can then browse the documentation with::

    make browse

Releasing a new version
-----------------------

- Bump the ``__version__`` value in ``tutor/__about__.py``.
- Replace "Latest" by the version name in CHANGELOG.md.
- Create a commit with the version changelog.
- ``git push``
- ``make release``

After a regular push to ``master``, run ``make nightly`` to update the "nightly" tag.
