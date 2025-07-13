(F6) EMMC
=========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_FLASH_02

   The board shall include a 4GB eMMC flash memory with reference ASFC4G31M-51 with High Speed DDR and HS200 support.

The following requirements are extracted from the datasheet of ASFC4G31M-51 [:ref:^DS2 <reftable>^].

Supply Voltages
^^^^^^^^^^^^^^^

.. requirement:: D_EMMC_01
   :rationale: This corresponds to an 8% precision arround 1.8V.
   :derivedfrom: U_FLASH_02

   The VCCQ supply voltage shall be within 1.70V and 1.95V with a current capacity of 120mA.

.. requirement:: D_EMMC_02
   :rationale: This corresponds to an 10% precision arround 3.3V.
   :derivedfrom: U_FLASH_02

   The VCC supply voltage shall be within 2.70V and 3.60V with a current capacity of 120mA.

.. requirement:: D_EMMC_03
   :derivedfrom: U_FLASH_02

   Both a 4.7uF and a 100nF capacitors shall be placed between VDDI and VSS.

.. requirement:: D_EMMC_04
   :derivedfrom: U_FLASH_02

   Both a 10uF and a 100nF capacitors shall be placed between VCC and VSS.

.. requirement:: D_EMMC_05
   :derivedfrom: U_FLASH_02

   Both a 4.7uF and a 100nF capacitors shall be placed between VCCQ and VSS.

.. requirement:: D_EMMC_6
   :derivedfrom: U_FLASH_02

   The following signals shall be routed with transmission lines matched to 50ohms : DAT0-DAT7, CMD and CLK.

.. requirement:: D_EMMC_7
   :derivedfrom: U_FLASH_02

   The following signals shall be length matched up to ±1mm : DAT0-DAT7, CMD and CLK.


Circuit diagram
---------------

Design calculations
-------------------

Simulation results
------------------

Pre-layout
``````````

The goal of the pre-layout simulation is to adjust the high-speed bus termination.

Transient behavior
^^^^^^^^^^^^^^^^^^

Eye Diagram
^^^^^^^^^^^

Post-layout
```````````

The goal of the post-layout simulation is to simulate the high-speed bus taking into account the routed trace geometry.

Transient behavior
^^^^^^^^^^^^^^^^^^

Eye Diagram
^^^^^^^^^^^

Crosstalk
^^^^^^^^^

Routing
-------

Length matching
```````````````

.. flat-table:: Signal trace length delay constraints
   :header-rows: 1
   :width: 100%

   * - Constraint
     - Description

   * - LC1
     - Mismatch within DAT0~DAT7+DS <= 41ps

   * - LC2
     - CLK to DAT0~7+DS mismatch <= 41ps

   * - LC3
     - CLK to CMD mismatch <= 41ps

   * - LC4
     - CLK to RST_N mismatch <= 166ps

.. note:: Signals applicable to LC1 will be matched to the longest one of them

All signals are routed on layers L1/L6 which share the same propagation speed, and the number of vias has been matched so the signals are length matched with 41ps leading to <= 7.246mm and 166ps leading to <= 29.337mm.

.. flat-table:: Length matching implementation
   :header-rows: 1
   :width: 100%

   * - Signal
     - Pre-matching Length
     - LC1
     - LC2
     - LC3
     - LC4
     - Matching target  
     - Post-matching length

   * - CLK
     - 17.8451mm
     - N/A
     - N/A
     - N/A
     - N/A
     - N/A
     - N/A

   * - CMD
     - 17.9620mm
     - N/A
     - N/A
     - Yes
     - N/A
     - N/A
     - N/A

   * - RST_N
     - 15.2397mm
     - N/A
     - N/A
     - N/A
     - Yes
     - N/A
     - N/A

   * - DS
     - 15.9327mm
     - Yes
     - Yes
     - N/A
     - N/A
     - N/A
     - N/A

   * - DAT0
     - 9.7788mm
     - Yes
     - No
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

   * - DAT1
     - 11.6159mm
     - Yes
     - Yes
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

   * - DAT2
     - 10.6077mm
     - Yes
     - Yes
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

   * - DAT3
     - 10.9396mm
     - Yes
     - Yes
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

   * - DAT4
     - 9.8626mm
     - Yes
     - No
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

   * - DAT5
     - 16.0556mm
     - Yes
     - Yes
     - N/A
     - N/A
     - N/A
     - N/A 

   * - DAT6
     - 16.7553mm
     - Longest
     - Yes
     - N/A
     - N/A
     - N/A
     - N/A

   * - DAT7
     - 13.4568mm
     - Yes
     - Yes
     - N/A
     - N/A
     - 14.223mm (Clk-Tol/2)
     - 14.223mm

