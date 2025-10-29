.. _versions:

Versions
========

Starting from ``v4.0.0``, ``pesptool`` adopts the `semantic versioning specification <https://semver.org/>`_, following the ``MAJOR.MINOR.PATCH`` version number.

Major release ``v4`` is under active development, receiving new features and bugfixes, while ``v3`` only keeps receiving important bugfixes.

There are no support periods defined and bugfixes are not planned, therefore it is strongly recommended to install the latest version possible.

.. note::

    The following information is directed mainly towards package maintainers. Regular users should always use the most recent version of ``pesptool`` to benefit from the latest features and bugfixes.

Use the Latest pesptool (Recommended)
------------------------------------

If your use case doesn't impose any constraints on ``pesptool``, the latest release should be always used.
To see the latest available version and its release notes, visit the `release page on GitHub <https://github.com/espressif/pesptool/releases>`_.

To get the latest possible version, simply define your dependency as ``pesptool`` (without any release operator and a version identifier).

Use the Latest Bugfix Release of a Minor pesptool Release
--------------------------------------------------------

Some use cases might require a specific ``pesptool`` version without getting new features, but with automatic bugfixes.

This can be achieved by defining your dependency as ``pesptool~=4.0.1`` (explicitly stating the ``MAJOR``, ``MINOR``, and ``PATCH`` numbers).
This notation selects the latest version of ``pesptool``, greater than or equal to ``v4.0.1``, but still in the ``v4.0.*`` version (this compatible release clause is approximately equivalent to the pair of comparison clauses ``>= 4.0.1``, ``== 4.0.*``).
So, for example, ``v4.1.0`` won't be downloaded. More information about compatible release clauses `can be found here <https://peps.python.org/pep-0440/#compatible-release>`_.

Use the Latest pesptool Without Any Future Breaking Change
---------------------------------------------------------

If you also want to get new features (instead of just bugfixes), define your version requirement as ``pesptool~=4.0`` (explicitly stating only the ``MAJOR`` and ``MINOR`` numbers). This way the latest minor versions (``>= 4.0``, ``== 4.*``) are automatically installed.
Backward-compatibility is still ensured, because ``pesptool`` respects the semantic versioning specification (which states that breaking changes should occur only in ``MAJOR`` versions).

Use the Previous Major pesptool Release (Only if You Cannot Upgrade)
-------------------------------------------------------------------

If your use case is not compatible with the latest ``MAJOR`` release of ``pesptool``, a previous compatible version has to be specified.
This can be achieved by defining your dependency as ``pesptool~=3.0`` (explicitly stating your desired ``MAJOR`` number and at least also the ``MINOR`` number, ``PATCH`` can also be specified).

Use a Specific pesptool Release
------------------------------

If a very specific release is required, define your dependency as ``pesptool==4.1.2``. This specific version will be used and no new features or bugfixes will be automatically installed.
