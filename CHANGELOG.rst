Changelog
=========

Versions follow `CalVer <http://calver.org>`_ with *no* backward-compatibility guarantees whatsoever.
The third digit is only for regressions.


21.3.0 (UNRELEASED)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Python 2.7, 3.5, and 3.6 support has been dropped.
  *environ-config* now requires Python 3.7 or later.


Deprecations:
^^^^^^^^^^^^^

*none*


Changes:
^^^^^^^^

- Lazily init the AWS SecretsManager client to make unit testing easier.
  `#25 <https://github.com/hynek/environ-config/pull/25>`_


----


21.2.0 (2021-05-17)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

*none*


Deprecations:
^^^^^^^^^^^^^

- This is the last release supporting Python versions older than 3.7.


Changes:
^^^^^^^^

- Added `AWS SecretsManager <https://aws.amazon.com/secrets-manager/>`_ support.
  `#23 <https://github.com/hynek/environ-config/pull/23>`_


----


21.1.0 (2021-04-14)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

*none*

Deprecations:
^^^^^^^^^^^^^

*none*


Changes:
^^^^^^^^

- Fixed environment variables' names when prefix is empty.
  `#14 <https://github.com/hynek/environ-config/pull/14>`_
- Added the ``optional`` keyword argument to ``environ.group()``
  `#17 <https://github.com/hynek/environ-config/pull/17>`_
- Added ``DirectorySecrets`` secret reader, which can read secrets from a directory of files.
  Useful for Docker or Kubernetes mounted secrets inside a container.
  `#19 <https://github.com/hynek/environ-config/pull/19>`_


----


20.1.0 (2020-03-23)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

*none*


Deprecations:
^^^^^^^^^^^^^

*none*


Changes:
^^^^^^^^

- Configurations can be immutable now.
  `#12 <https://github.com/hynek/environ-config/issues/12>`_


----


19.1.0 (2019-09-02)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Changed license from MIT to Apache License 2.


Deprecations:
^^^^^^^^^^^^^

*none*


Changes:
^^^^^^^^

- Added ``AppConfig.from_environ()`` to instantiate the configuration class.
  This is an alternative to ``environ.from_environ(AppConfig)``.
  `#5 <https://github.com/hynek/environ-config/issues/5>`_
- Added ``environ.generate_help(AppConfig)`` and ``AppConfig.generate_help()`` to create a help string based on the configuration.
- Allow passing customization of the ``"from_environ"`` and ``"generate_help"`` class methods.
  `#7 <https://github.com/hynek/environ-config/issues/7>`_
- If ``environ.var`` is passed an ``attr.Factory``, the callable is used to generate the default value.
  `#10 <https://github.com/hynek/environ-config/issues/10>`_


----


18.2.0 (2018-01-12)
-------------------

Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Use ``RawConfigParser`` for ini-style secrets to avoid interpolation errors.


Changes:
^^^^^^^^

*none*


----

18.1.0 (2018-01-04)
-------------------


Backward-incompatible changes:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- ``convert`` → ``converter``


Changes:
^^^^^^^^

- Fix for ``attrs`` 17.4.0.


----


17.1.0 (2017-12-14)
-------------------

Initial release.
