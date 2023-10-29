Установка Zerotier
=====

Установка с официального сайта блокируется с IP из России.

Используйте VPN для обхода ограничений или можно собрать приложение по инструкции

.. _installation_linux_easy:

Ubuntu 22.04 (не из России)
------------
.. tip::

    Самый простой способ, если есть VPN в другую страну

Следуем инструкции официального сайта `Zerotier <https://www.zerotier.com/download/>`_

.. code-block:: console

    curl -s https://install.zerotier.com | sudo bash


.. _installation_linux:

Ubuntu 22.04 (Вручную)
------------
.. tip::

    Лучше все команды выполнять в режиме суперпользователя (sudo -i)

Устанавливаем зависимости которые понадобятся для сборки

.. code-block:: console

    apt update && apt install libssl-dev pkg-config build-essential git


Загружаем Rust для компиляции, выбираем 1) default установку

.. code-block:: console

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh


Обновляем переменную окружения

.. code-block:: console

    source "$HOME/.cargo/env"


Клонируем официальный репозиторий Zerotier

.. code-block:: console

    git clone https://github.com/zerotier/ZeroTierOne && cd ZeroTierOne

Собираем приложение и устанавливаем

.. code-block:: console

    make && make install


Запускаем демон приложения

.. code-block:: console

    zerotier-one -d

.. _installation_windows:

Windows 10/11
------------

Скачиваем MSI установщик с официального сайта - `скачать <https://download.zerotier.com/dist/ZeroTier%20One.msi>`_