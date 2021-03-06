An index cannot |cover| a query on a :term:`sharded <shard>` collection
when run against a :program:`mongos` if the index does not contain the
shard key, with the following exception for the ``_id`` index: If a
query on a sharded collection only specifies a condition on the ``_id``
field and returns only the ``_id`` field, the ``_id`` index can cover
the query when run against a :program:`mongos` even if the ``_id``
field is not the shard key.

.. versionchanged:: 3.0

   In previous versions, an index cannot :ref:`cover <covered-queries>`
   a query on a :term:`sharded <shard>` collection when run against a
   :program:`mongos`.
