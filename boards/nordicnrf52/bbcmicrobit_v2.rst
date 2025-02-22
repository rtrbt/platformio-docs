..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_nordicnrf52_bbcmicrobit_v2:

BBC micro:bit V2
================

.. contents::

Hardware
--------

Platform :ref:`platform_nordicnrf52`: The nRF52 Series are built for speed to carry out increasingly complex tasks in the shortest possible time and return to sleep, conserving precious battery power. They have a Cortex-M4F processor which makes them quite capable Bluetooth Smart SoCs.

.. list-table::

  * - **Microcontroller**
    - NRF52833
  * - **Frequency**
    - 64MHz
  * - **Flash**
    - 512KB
  * - **RAM**
    - 128KB
  * - **Vendor**
    - `BBC <https://microbit.org/new-microbit/?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``bbcmicrobit_v2`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:bbcmicrobit_v2]
  platform = nordicnrf52
  board = bbcmicrobit_v2

You can override default BBC micro:bit V2 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `bbcmicrobit_v2.json <https://github.com/platformio/platform-nordicnrf52/blob/master/boards/bbcmicrobit_v2.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:bbcmicrobit_v2]
  platform = nordicnrf52
  board = bbcmicrobit_v2

  ; change microcontroller
  board_build.mcu = nrf52833

  ; change MCU frequency
  board_build.f_cpu = 64000000L


Uploading
---------
BBC micro:bit V2 supports the following uploading protocols:

* ``blackmagic``
* ``cmsis-dap``
* ``jlink``
* ``mbed``
* ``nrfjprog``
* ``stlink``

Default protocol is ``cmsis-dap``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:bbcmicrobit_v2]
  platform = nordicnrf52
  board = bbcmicrobit_v2

  upload_protocol = cmsis-dap

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

BBC micro:bit V2 has on-board debug probe and **IS READY** for debugging. You don't need to use/buy external debug probe.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_blackmagic`
    - 
    - 
  * - :ref:`debugging_tool_cmsis-dap`
    - Yes
    - Yes
  * - :ref:`debugging_tool_jlink`
    - 
    - 
  * - :ref:`debugging_tool_stlink`
    - 
    - 

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_arduino`
      - Arduino Wiring-based Framework allows writing cross-platform software to control devices attached to a wide range of Arduino boards to create all kinds of creative coding, interactive objects, spaces or physical experiences

    * - :ref:`framework_zephyr`
      - The Zephyr Project is a scalable real-time operating system (RTOS) supporting multiple hardware architectures, optimized for resource constrained devices, and built with safety and security in mind