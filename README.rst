multigtfs: GTFS as a Django app
===============================

.. image:: https://img.shields.io/pypi/v/multigtfs.svg
    :alt: The PyPI package
    :target: https://pypi.python.org/pypi/multigtfs

.. image:: https://img.shields.io/pypi/dw/multigtfs.svg
    :alt: PyPI download statistics
    :target: https://pypi.python.org/pypi/multigtfs

.. image:: https://img.shields.io/travis/tulsawebdevs/django-multi-gtfs/master.svg
    :alt: TravisCI Build Status
    :target: https://travis-ci.org/tulsawebdevs/django-multi-gtfs

.. image:: https://img.shields.io/coveralls/tulsawebdevs/django-multi-gtfs/master.svg
    :alt: Coveralls Test Coverage
    :target: https://coveralls.io/r/tulsawebdevs/django-multi-gtfs?branch=master

.. Omit badges from docs

**multigtfs** is an `Apache 2.0`_-licensed Django app that supports importing
and exporting of GTFS feeds.  All features of the `June 20, 2012 reference`_
are supported, including `all changes`_ up to February 17, 2014.
It allows multiple feeds to be stored in the database at once.

It requires a spatial databases compatible with GeoDjango_.  PostgreSQL_ 9.x
and PostGIS_ 2.x are recommended for development and production, since these
support all the GeoDjango features.

Status
------
multigtfs is ready for your GTFS project.

Point releases (such as 1.0.0 to 1.0.1) should be safe, only adding features or
fixing bugs.  Minor updates (1.0.1 to 1.1.0) may include significant changes
that will break relying code.  In the worst case scenario, you may need to
export your GTFS feeds in the original version, update multigtfs and your code,
and re-import.

multigtfs works with Django 1.8 (the long-term support, or LTS, release)
through 1.10.  Support will follow the Django supported releases, as well as
the Python versions supported by those releases.

All valid GTFS feeds are supported for import and export.  This includes
feeds with extra columns not yet included in the GTFS spec, and feeds that
omit ``calendar.txt`` in favor of ``calendar_dates.txt`` (such as the TriMet
archive feeds).  If you find a feed that doesn't work, `file a bug`_!

See the `issues list`_ for more details on bugs and feature requests.

Example project
---------------
Check out the `example project <examples/explore/README.md>`_.

Development
-----------

:Code:           https://github.com/tulsawebdevs/django-multi-gtfs
:Issues:         https://github.com/tulsawebdevs/django-multi-gtfs/issues
:Dev Docs:       http://multigtfs.readthedocs.org/
:IRC:            irc://irc.freenode.net/tulsawebdevs


.. _`Apache 2.0`: http://choosealicense.com/licenses/apache/
.. _`June 20, 2012 reference`: https://developers.google.com/transit/gtfs/reference
.. _`all changes`: https://developers.google.com/transit/gtfs/changes#RevisionHistory
.. _PostgreSQL: http://www.postgresql.org
.. _PostGIS: http://postgis.refractions.net
.. _GeoDjango: https://docs.djangoproject.com/en/dev/ref/contrib/gis/
.. _`file a bug`: https://github.com/tulsawebdevs/django-multi-gtfs/issues
.. _`issues list`: https://github.com/tulsawebdevs/django-multi-gtfs/issues?state=open
