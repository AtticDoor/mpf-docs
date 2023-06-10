segment_displays:
=================

*Config file section*

+----------------------------------------------------------------------------+---------+
| Valid in :doc:`machine config files </config/instructions/machine_config>` | **YES** |
+----------------------------------------------------------------------------+---------+
| Valid in :doc:`mode config files </config/instructions/mode_config>`       | **NO**  |
+----------------------------------------------------------------------------+---------+

.. overview

The ``segment_displays:`` section of your config is where you define your
:doc:`segment displays </displays/display/alpha_numeric>`.
This can be 7-segment or alphanumeric displays which are typically
used in older machines.

.. config


Required settings
-----------------

The following sections are required in the ``segment_displays:`` section of your config:

number:
~~~~~~~
Single value, type: ``string``. Defaults to empty.

The number of the display. The meaning depends on the hardware platform.


Optional settings
-----------------

The following sections are optional in the ``segment_displays:`` section of your config. (If you don't include them, the default will be used).

default_color:
~~~~~~~~~~~~~~
List of one (or more) values, each is a type: ``color`` (*color name*, *hex*, or list of values *0*-*255*). Default: ``white``

.. todo:: :doc:`/about/help_us_to_write_it`

default_transition_update_hz:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Single value, type: float_or_token. Default: ``30``

The speed (steps per second) at which text transition effects will be updated in the display.

integrated_commas:
~~~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (``true``/``false``). Default: ``false``

Determines whether or not the physical segment display has integrated commas in each character rather than taking
up an entire character. When set to ``true``, commas are collapsed with the preceding character when calculating
text transition effects.

integrated_dots:
~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (``true``/``false``). Default: ``false``

Determines whether or not the physical segment display has integrated dots/periods in each character rather than
taking up an entire character. When set to ``true``, dots/periods are collapsed with the preceding character when
calculating text transition effects.

platform:
~~~~~~~~~
Single value, type: ``string``. Defaults to empty.

This can be used to overwrite the platform which is defined in the *hardware*
section for segment_displays.

platform_settings:
~~~~~~~~~~~~~~~~~~
Single value, type: dict. Defaults to empty.

Platform specific settings.
See your :doc:`segment platform documentation </hardware/segment_display_platforms>`.

size:
~~~~~
Single value, type: ``integer``. Default: ``7``

The number of characters in the segment display. This value should be set to match the number of characters in
your physical hardware (or virtual emulator). It is important to set this number correctly for the text
transition effects.

use_dots_for_commas:
~~~~~~~~~~~~~~~~~~~~
Single value, type: ``boolean`` (``true``/``false``). Default: ``false``

.. todo:: :doc:`/about/help_us_to_write_it`

console_log:
~~~~~~~~~~~~
Single value, type: one of the following options: none, basic, full. Default: ``basic``

Log level for the console log for this device.

debug:
~~~~~~
Single value, type: ``boolean`` (``true``/``false``). Default: ``false``

Set this to true to see additional debug output. This might impact the performance of MPF.

file_log:
~~~~~~~~~
Single value, type: one of the following options: none, basic, full. Default: ``basic``

Log level for the file log for this device.

label:
~~~~~~
Single value, type: ``string``. Default: ``%``

Name of this device in service mode.

tags:
~~~~~
List of one (or more) values, each is a type: ``string``. Defaults to empty.

Not used.


Related How To guides
---------------------

* :doc:`/displays/display/alpha_numeric`
* :doc:`/hardware/segment_display_platforms`
