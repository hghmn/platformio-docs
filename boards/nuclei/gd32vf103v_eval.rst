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

.. _board_nuclei_gd32vf103v_eval:

GD32VF103V Evaluation Kit
=========================

.. contents::

Hardware
--------

Platform :ref:`platform_nuclei`: Find professional RISC-V Processor IP in Nuclei, first professional RISC-V IP company in Mainland China, match all your requirements in AIoT Era.

.. list-table::

  * - **Microcontroller**
    - GD32VF103VBT6
  * - **Frequency**
    - 108MHz
  * - **Flash**
    - 128KB
  * - **RAM**
    - 32KB
  * - **Vendor**
    - `GigaDevice <https://www.gigadevice.com/?utm_source=platformio&utm_medium=docs>`__


Configuration
-------------

Please use ``gd32vf103v_eval`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:gd32vf103v_eval]
  platform = nuclei
  board = gd32vf103v_eval

You can override default GD32VF103V Evaluation Kit settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `gd32vf103v_eval.json <https://github.com/Nuclei-Software/platform-nuclei/blob/master/boards/gd32vf103v_eval.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:gd32vf103v_eval]
  platform = nuclei
  board = gd32vf103v_eval

  ; change microcontroller
  board_build.mcu = gd32vf103vbt6

  ; change MCU frequency
  board_build.f_cpu = 108000000L


Uploading
---------
GD32VF103V Evaluation Kit supports the next uploading protocols:

* ``altera-usb-blaster``
* ``gd-link``
* ``jlink``
* ``rv-link``

Default protocol is ``rv-link``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:gd32vf103v_eval]
  platform = nuclei
  board = gd32vf103v_eval

  upload_protocol = rv-link

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

GD32VF103V Evaluation Kit does not have on-board debug probe and **IS NOT READY** for debugging. You will need to use/buy one of external probe listed below.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_altera-usb-blaster`
    - 
    - Yes
  * - :ref:`debugging_tool_gd-link`
    - 
    - 
  * - :ref:`debugging_tool_jlink`
    - 
    - 
  * - :ref:`debugging_tool_rv-link`
    - 
    - 

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_nuclei-sdk`
      - Open Source Software Development Kit for the Nuclei N/NX processors