Подключение к сети
===
Адрес нашей сети **96bd2850de30cbbd**

.. _connection_windows:

Запускаем программу ZeroTier. Сервис должен появится в трее.

Нажимаем Join network, указываем адрес: || 96bd2850de30cbbd

Обязательно ставим галку напротив параметра Allow Default Router Override

Написать в `Telegram <https://t.me/pgsq1>`_ @pgsq1 номер своего адреса сети (наверху панели)

.. _connection_linux_bash:

Подключаемся к сети
.. code-block:: console

   sudo zerotier-cli join 96bd2850de30cbbd

Написать в `Telegram <https://t.me/pgsq1>`_ @pgsq1 номер своего адреса сети, номер идет после 200 info

.. code-block:: console

   sudo zerotier-cli info

