(F7) FLASH
==========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_FLASH_01
   :rationale: Only 32MBits are required to store the FPGA bitstream but the extra storage can be used by the user more easily than the eMMC. This reference supports optional programmable QSPI interface.

   The board shall include a 128Mbits NOR flash memory with reference W25Q128JVPIM to store the FPGA bitstream used in Quad-SPI configuration.

The following requirements are extracted from the datasheet of W25Q128JVPIM [:ref:^DS1 <reftable>^].

.. requirement:: D_FLASH_01
   :rationale: This corresponds to a 10% precision arround 3.3V.
   :derivedfrom: U_FLASH_01

   The VCC supply voltage shall be within 3.0V and 3.6V with a current capacity of 25mA.

.. requirement:: D_FLASH_02
   :derivedfrom: U_FLASH_01

   The CS input shall track the VCC supply levet at power-up and power-down using a pull-up resistor.

.. requirement:: D_FLASH_03
   :derivedfrom: U_FLASH_01

   The time between VCC reaching 3.0V to the CS pin being pulled low shall be at least 20us.

This requirement implies that the FPGA must not start its configuration before 20us after VCC reaches 3.0V.

.. requirement:: D_FLASH_04
   :derivedfrom: U_FLASH_01

   The time between VCC reaching 2.0V and the first write instruction shall be at least 5ms.

This requirement is only provided as information as write operations are only performed by the board designer while the board is already up and running.


Circuit diagram
---------------

Design calculations
-------------------

Simulation results
------------------
