SSH Tips and Tricks
###################

SSH Escape Sequences
--------------------

An escape sequence can be sent to your **local** SSH client while connected to
a remote server by pressing ``<Enter>``, ``~``, then an appropriate key for a
particular sequence.

* ``<Enter>``, ``~``, ``?`` - display a list of supported sequences
* ``<Enter>``, ``~``, ``.`` - terminate connection (and any multiplexed sessions)
* ``<Enter>``, ``~``, ``B`` - send a BREAK to the remote system
* ``<Enter>``, ``~``, ``C`` - open a command line (see ``SSH Commands``_)
* ``<Enter>``, ``~``, ``R`` - Request rekey
* ``<Enter>``, ``~``, ``^Z`` - suspend ssh (this is ``<Ctrl>``+``Z``)
* ``<Enter>``, ``~``, ``#`` - list forwarded connections
* ``<Enter>``, ``~``, ``&`` - background ssh (when waiting for connection to terminate)
* ``<Enter>``, ``~``, ``~`` - send the escape character by typing it twice


Rescue Frozen Bash from disconnected SSH session
------------------------------------------------

When an SSH session is disconnected for whatever reason, sometimes bash will
freeze. Bash can be unfozen by sending the SSH escape sequence, which by default
is: ``~``.

The escape sequence can be sent by pressing: ``<Enter>``, ``~``, and then ``.``.


SSH Commands
------------

These commands can be run while already connected via ssh to a remote server
using the escape sequence: ``<Enter>``, ``~``, and then ``C``.

* ``-L[bind_address:]port:host:hostport`` - Request local forward
* ``-R[bind_address:]port:host:hostport`` - Request remote forward
* ``-D[bind_address:]port`` - Request dynamic forward
* ``-KR[bind_address:]port`` - Cancel remote forward


----

This work is licensed under a `Creative Commons Attribution 4.0 International License <http://creativecommons.org/licenses/by/4.0>`_.

.. image:: https://i.creativecommons.org/l/by/4.0/88x31.png
    :target: http://creativecommons.org/licenses/by/4.0/

Copyright (c) 2016 Harold Bradley III

----

*Soli Deo gloria.*
