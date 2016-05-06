Bash Terminal Tips and Tricks
#############################

*Helpful commands and tricks for using the terminal more effectively.*

History Expansion
=================


Refering to Previous Commands or Arguments
------------------------------------------

.. code:: bash

      # Refer to the previous command
    $ !!
      # -or-
    $ !-1

      # Refer to a command 'n' lines back
    $ !-n  # Replace 'n' with a number
    $ !-3

      # Refer to a previous command starting with 'string'
    $ !string

      # Refer to a previous command containing 'string'
    $ !?string

      # History with Substitution:
    $ echo 'hi'
    hi
      # Replaces 'hi' with 'hello'
    $ !!:s/hi/hello/
    hello

      # Refer to the entire line typed so far:
    $ !#


      # Refer to the last argument of the preceding command
    $ !$
      # -or-
    $ !!:$


.. code:: bash

      # Empty a file (creates it if it doesn't exist)
    $ > file.txt

    $ cp /path/to/file{,_copy}

    $ mv /path/to/file{,_old}

    $ mv /path/{1,2}/file

    $ mv /path/{old/path,new/longer/path/}/file

Resources
===============

    - http://www.ukuug.org/events/linux2003/papers/bash_tips/
    - http://www.gnu.org/software/bash/manual/html_node/Word-Designators.html#Word-Designators


----

This work is licensed under a `Creative Commons Attribution 4.0 International License <http://creativecommons.org/licenses/by/4.0>`_.

.. image:: https://i.creativecommons.org/l/by/4.0/88x31.png
    :target: http://creativecommons.org/licenses/by/4.0/

Copyright (c) 2016 Harold Bradley III

----

*Soli Deo gloria.*
