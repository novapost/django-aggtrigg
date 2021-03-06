############
Contributing
############

This document provides guidelines for people who want to contribute to the
`django-aggtrigg` project.


**************
Create tickets
**************

Please use `django-aggtrigg bugtracker`_ **before** starting some work:

* check if the bug or feature request has already been filed. It may have been
  answered too!

* else create a new ticket.

* if you plan to contribute, tell us, so that we are given an opportunity to
  give feedback as soon as possible.

* Then, in your commit messages, reference the ticket with some
  ``refs #TICKET-ID`` syntax.


******************
Use topic branches
******************

* Work in branches.

* Please never push in ``master`` directly.

* Prefix your branch with one the following keyword ``feature/`` when
  adding a new feature and ``fix/`` when working on a fix.
  You can also add the ticket ID corresponding to the issue to be explicit.

* If you work in a development branch and want to refresh it with changes from
  master, please `rebase`_ or `merge-based rebase`_, i.e. do not merge master.


***********
Fork, clone
***********

Clone `django-aggtrigg` repository (adapt to use your own fork):

.. code:: sh

   git clone git@github.com:novafloss/django-aggtrigg.git
   cd django-aggtrigg/


*************
Usual actions
*************

The `Makefile` is the reference card for usual actions in development
environment:

* Install development toolkit with `pip`_: ``make develop``.

* Run tests with `tox`_: ``make test``.

* Build documentation: ``make documentation``. It builds `Sphinx`_
  documentation in `var/docs/html/index.html`.

* Release `django-aggtrigg` project with `zest.releaser`_: ``make release``.

* Cleanup local repository: ``make clean``, ``make distclean`` and
  ``make maintainer-clean``.

See also ``make help``.

****************
Test environment
****************

To get your test environment ready, you'll need at least an access to a 9.x
postgresql server. You may want to provide credentials, by editing the
`settings_local.sample.py` file and save it as `settings_local.py`
in the demo directory.

.. rubric:: Notes & references

.. target-notes::

.. _`django-aggtrigg bugtracker`: https://github.com/novafloss/django-aggtrigg/issues
.. _`rebase`: http://git-scm.com/book/en/v2/Git-Branching-Rebasing
.. _`merge-based rebase`: http://git-scm.com/book/en/v2/Git-Branching-Rebasing
.. _`pip`: https://pypi.python.org/pypi/pip/
.. _`tox`: https://pypi.python.org/pypi/tox/
.. _`Sphinx`: https://pypi.python.org/pypi/Sphinx/
.. _`zest.releaser`: https://pypi.python.org/pypi/zest.releaser/
