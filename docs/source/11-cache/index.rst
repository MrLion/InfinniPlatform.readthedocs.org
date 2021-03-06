Кэширование данных
==================

Кэширование позволяет экономить время на генерацию часто запрашиваемых статичных данных.
InfinniPlatform предоставляет возможность работы с двуми видами кэша:

#. Кэш в памяти (Memory).
#. Распределенный кэш (Shared).

Кэш в памяти
~~~~~~~~~~~~

Кэш хранится в памяти и очищается при остановке приложения.

Распределенный кэш
~~~~~~~~~~~~~~~~~~

.. important:: Для работы распределенного кэша требуется установленные Redis (см. :doc:`/11-cache/redis-install`) и RabbitMQ (см. :doc:`/12-queues/queues-install`).

Кэш хранится в памяти и дублируется в базе данных Redis. Таким образом, кэш может быть использован другими экземплярами приложения
и соответственно позволяет разворачивать приложения в кластере.

.. toctree::

    redis-install.rst
    cache-examples.rst