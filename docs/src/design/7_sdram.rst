(F4) SDRAM
==========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_MEMORY_02

   The board shall include two 16M x 16bits 256Mb Synchronous DRAM with reference IS42S16160J up to -6 speed grade.

The following requirements are extracted from the datasheet of IS42S16160J [:ref:^DS4 <reftable>^].

.. requirement:: D_SDRAM_01
   :rationale: This corresponds to an 10% precision arround 3.3V.
   :derivedfrom: U_MEMORY_02

   The VDD and VCCQ supply voltage shall be within 3.0V and 3.6V with a current capacity of 140mA x2.

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

Pre-layout
``````````

The goal of the pre-layout simulation is to adjust the high-speed bus termination.

The address and command trace stubs associated to the fly-by routing topology shall be smaller than 0.3/0.1Gbps = 3inch so no terminating resistors are needed.

Transient behavior
^^^^^^^^^^^^^^^^^^

.. note:: No signal-integrity simulations are performed for revision 1.0.0

Eye Diagram
^^^^^^^^^^^

.. note:: No signal-integrity simulations are performed for revision 1.0.0

Post-layout
```````````

The goal of the post-layout simulation is to simulate the high-speed bus taking into account the routed trace geometry.

Transient behavior
^^^^^^^^^^^^^^^^^^

.. note:: No signal-integrity simulations are performed for revision 1.0.0

Eye Diagram
^^^^^^^^^^^

.. note:: No signal-integrity simulations are performed for revision 1.0.0

Crosstalk
^^^^^^^^^

.. note:: No signal-integrity simulations are performed for revision 1.0.0

Routing
-------

Length matching
```````````````

According to AN42S01 "ISSI SRAM/SDRAM Layout Guide", the longest-to-shortest trace length difference shall be matched to <20.32mm (800mils).

For SDRAM1, the signals are all point-to-point with a maximum trace length difference of (16.93mm-5.3836) = 11.5464mm.

For SDRAM0, some signals are point-to-point whereas the address bus is shared with SDRAM1 and is therefore much longer.

.. flat-table:: Address bus trace length to SDRAM0
   :header-rows: 1
   :width: 100%

   * - Signal
     - Traces
     - Length

   * - A0 
     - 12.0144 + 10.4529
     - 22.4673mm

   * - A1 
     - 12.3720 + 11.0783 
     - 23.4503mm

   * - A2 
     - 12.7545 + 10.3013 
     - 23.0558mm

   * - A3
     - 12.5851 + 10.2281 
     - 22.8132mm

   * - A4 
     - 12.1668 + 10.2658 
     - 22.4326mm

   * - A5 
     - 10.9060 + 13.4390 
     - 24.345mm

   * - A6 
     - 10.6935 + 14.3101 
     - 25.0036mm

   * - A7 
     - 11.2030 + 13.5777 
     - 24.7807mm

   * - A8 
     - 10.9296 + 16.0072 
     - 26.9368mm

   * - A9 
     - 10.7349 + 11.3978 
     - 22.1327mm

   * - A10 
     - 12.3981 + 9.6156 
     - 22.0137mm

   * - A11 
     - 10.6521 + 13.3707 
     - 24.0228mm

   * - A12
     - 11.2846 + 14.6813 
     - 25.9659mm

   * - BA0
     - 13.8279 + 12.6978 
     - 26.5257mm

   * - BA1
     - 12.7992 + 8.8939 
     - 21.6931mm

The signals shall be longer than 7mm.
