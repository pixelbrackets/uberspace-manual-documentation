.. _mailfilters:

###############
Filtering mails
###############

We filter incoming mails with `Rspamd <https://rspamd.com>`_ which uses `multiple <https://rspamd.com/comparison.html>`_ filtering and statistical methods to generate a spam score, including (but not limited to) SPF, DMARC and DNS blacklists. Mails with a score greater than 15 get rejected. 

Configure spam filter
=====================

Use ``uberspace mail spamfilter`` to configure the filter for your account:

.. code-block:: console

  [eliza@dolittle ~]$ uberspace mail spamfilter status
  Mail filter enabled.
  [eliza@dolittle ~]$ uberspace mail spamfilter disable
  Mail filter disabled.
  [eliza@dolittle ~]$ uberspace mail spamfilter enable
  Mail filter enabled.

Header
======

We add the score to the mail header: ``X-Rspamd-Bar``, ``X-Rspamd-Report`` and ``X-Rspamd-Score``.
