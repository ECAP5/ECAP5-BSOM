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
