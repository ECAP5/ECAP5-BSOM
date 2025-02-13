(F8) CLOCK
==========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_OSC_01
   :rationale: 40MHz LVCMOS, Enable/Disable on pin 1, 3.2x2.5mm package, 3.3VDC±5% supply, ±50ppm precision, -40 to +85°C temperature range.

   A 40 MHz reference oscillator shall be connected to one of the FPGA's global clock inputs, with reference XLH335040.000000I.

The following requirements are extracted from the datasheet of XLH736030.000000I [:ref:^DS6 <reftable>^].

Supply Voltage
^^^^^^^^^^^^^^

.. requirement:: D_OSC_01
   :derivedfrom: U_OSC_01

   The VDD supply voltage shall be within 3.135V and 3.465V with a current capacity of 35mA.

.. requirement:: D_OSC_02
   :derivedfrom: U_OSC_01

   A 0.01uF bypass capacitor shall be placed between VDD and GND.


Circuit diagram
---------------

Design calculations
-------------------

Simulation results
------------------
