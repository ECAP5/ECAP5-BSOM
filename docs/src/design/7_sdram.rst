(F4) SDRAM
==========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_MEMORY_02

   The board shall include a 16M x 16bits 256Mb Synchronous DRAM with reference IS42S16160J up to -6 speed grade.

The following requirements are extracted from the datasheet of IS42S16160J [:ref:^DS4 <reftable>^].

.. requirement:: D_SDRAM_01
   :rationale: This corresponds to an 10% precision arround 3.3V.
   :derivedfrom: U_MEMORY_02

   The VDD and VCCQ supply voltage shall be within 3.0V and 3.6V with a current capacity of 140mA.

.. requirement:: D_SDRAM_02
   :derivedfrom: U_MEMORY_02

   The following pins shall not exceed VDD+0.3V : Address, Data and Control pins.

.. requirement:: D_SDRAM_03
   :derivedfrom: U_MEMORY_02

   The following pins shall not be lower than -0.3V : Address, Data and Control pins.

Circuit diagram
---------------

Design calculations
-------------------

Simulation results
------------------
