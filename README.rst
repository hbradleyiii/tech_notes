Terminal Tricks
###############
**Helpful commands and tricks for using the terminal more effectively.**
----

Terminal Tricks
===============

Working with Log Files
----------------------

Log file that has gotten too large:

.. code:: bash

    $ # How many lines?
    $ wc -l error.log
    7031689 error.log

    $ # View the most recent 2000 lines
    $ tail -n 2000 error.log | less
    ...

    $ # Delete all but most recent lines
    $ # !! Caution: permanently deletes data !!
    $ sed -i 1,7029000d error.log


Security
========

Finding Malicious Code
----------------------

Often I've found that malicious shell code has really long lines. Usually, it is easier to sort through a relatively few number of legitimate long lines to find malicious code.

.. code:: bash

    $ find ./ -type f -not -name '*.js' \
      -not -name '*.jpg' \
      -not -name '*.png' \
      -not -name '*.css' \
      -not -name '*.gif' \
      -not -name '*.svg' \
      -not -name '*.pdf' \
      -exec grep -En '.{800}' {} + | less


----

This work is licensed under a `Creative Commons Attribution 4.0 International License <http://creativecommons.org/licenses/by/4.0>`_.

.. image:: https://i.creativecommons.org/l/by/4.0/88x31.png
    :target: http://creativecommons.org/licenses/by/4.0/

Copyright (c) 2016 Harold Bradley III

----

*Soli Deo gloria.*
