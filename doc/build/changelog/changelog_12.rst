==============
1.2 Changelog
==============

.. changelog_imports::

    .. include:: changelog_11.rst
        :start-line: 5

    .. include:: changelog_10.rst
        :start-line: 5

.. changelog::
    :version: 1.2.0b1


    .. change:: 3276
        :tags: bug, oracle
        :tickets: 3276

        Oracle reflection now "normalizes" the name given to a foreign key
        constraint, that is, returns it as all lower case for a case
        insensitive name.  This was already the behavior for indexes
        and primary key constraints as well as all table and column names.
        This will allow Alembic autogenerate scripts to compare and render
        foreign key constraint names correctly when initially specified
        as case insensitive.

        .. seealso::

            :ref:`change_3276`