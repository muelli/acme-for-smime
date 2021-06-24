ACME for S/MIME
==================


This document lists the artefact we have created to implement an end-to-end
ACME for S/MIME scenario s.t. a Thunderbird user can acquire an S/MIME certificate
through the ACME for S/MIME protocol as per RFC8823.

Patches
~~~~~~~~~~

We have modified Pebble, acme-tiny, and Thunderbird.


Pebble
--------

We have modified Pebble 2.3.1.
See this repository for details: https://github.com/AzetinnitezA/pebble/tree/experimental_s-mime_support.
Our modifications include the ability to send and receive emails.
For our setup, we use Greenmail: https://greenmail-mail-test.github.io/greenmail/


acme-tiny
------------

Our modifications to acme-tiny are here: https://github.com/AzetinnitezA/acme-tiny/tree/acme_tiny_s-mime_support.
They add support for sending and receiving emails.


Thunderbird
-------------

Building Thunderbird is a bit of a pain.
We have had success basing our build on the flatpaked version: https://github.com/flathub/org.mozilla.Thunderbird.
Our patch is in this repository as acmesmime.patch.
Our patch can be applied on THUNDERBIRD_78_7_1_RELEASE: https://hg.mozilla.org/releases/comm-esr78/log?rev=1ef5b612ee43c806752ca215b142a9733210f3cc.


