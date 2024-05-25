Requirements
============

Flash
-----

The following requirements are extracted from the datasheet of W25Q128JVPIM [:ref:`DS1 <reftable>`].

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

eMMC
----

The following requirements are extracted from the datasheet of THGBMJG6C1LBAIL [:ref:`DS2 <reftable>`].

Supply
^^^^^^

.. requirement:: D_EMMC_01
   :rationale: This corresponds to an 8% precision arround 1.8V.
   :derivedfrom: U_FLASH_02

   The VCCQ supply voltage shall be within 1.70V and 1.95V with a current capacity of 220mA.

.. requirement:: D_EMMC_02
   :rationale: This corresponds to an 10% precision arround 3.3V.
   :derivedfrom: U_FLASH_02

   The VCC supply voltage shall be within 2.70V and 3.60V with a current capacity of 40mA.

.. requirement:: D_EMMC_03
   :derivedfrom: U_FLASH_02

   A 2.2uF capacitor shall be placed between VDDI and VSS.

.. requirement:: D_EMMC_04
   :derivedfrom: U_FLASH_02

   Both a 2.2uF and a 100nF capacitors shall be placed between VCC and VSS.

.. requirement:: D_EMMC_05
   :derivedfrom: U_FLASH_02

   Both a 2.2uF and a 100nF capacitors shall be placed between VCCQ and VSS.

.. requirement:: D_EMMC_06
   :derivedfrom: U_FLASH_02

   The time between VCCQ reaching 1.70V and VCC reaching 2.70V shall be less than 80ms.


Interface
^^^^^^^^^

.. requirement:: D_EMMC_07
   :derivedfrom: U_FLASH_02

   A 4.7kohms to 50kohms pull-up resistor shall be placed between the CMD pin and VCCQ.

.. requirement:: D_EMMC_08
   :derivedfrom: U_FLASH_02

   A 10kohms to 50kohms pull-up resistor shall be placed between the DAT0-DAT7 pins and VCCQ.

.. requirement:: D_EMMC_09
   :derivedfrom: U_FLASH_02

   A 10kohms to 50kohms pull-down resistor shall be placed between the Data Strobe pin and VSSQ.

.. requirement:: D_EMMC_10
   :derivedfrom: U_FLASH_02

   A 10kohms pull-up resistor shall be placed between the RST_n pin and VCCQ.

.. requirement:: D_EMMC_11
   :derivedfrom: U_FLASH_02

   The following signals shall be routed with transmission lines matched to 50ohms ±10% : DAT0-DAT7, CMD and CLK.

.. requirement:: D_EMMC_12
   :derivedfrom: U_FLASH_02

   The 47ohms termination resistor shall be placed in series with the following signals : CLK, CMD, DS, DAT0-DAT7 and RST_n.

.. requirement:: D_EMMC_13
   :derivedfrom: U_FLASH_02

   The following signals shall be length matched : DAT0-DAT7, CMD and CLK.

.. todo:: Simulate the Signal integrity with and without the termination resistors.

SRAM
----

SDRAM
-----

DDR2
----

FPGA
----
