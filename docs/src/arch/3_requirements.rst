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

SRAM
----

The following requirements are extracted from the datasheet of IS61WV25616BLL [:ref:`DS3 <reftable>`].

.. requirement:: D_SRAM_01
   :rationale: This corresponds to an 5% precision arround 3.3V.
   :derivedfrom: U_MEMORY_01

   The VDD supply voltage shall be within 3.135V and 3.465V with a current capacity of 50mA.

.. requirement:: D_SRAM_02
   :derivedfrom: U_MEMORY_01

   The following pins shall not exceed VDD+0.3V : Address, Data and Control pins.

.. requirement:: D_SRAM_03
   :derivedfrom: U_MEMORY_01

   The following pins shall not be lower than -0.3V : Address, Data and Control pins.

SDRAM
-----

The following requirements are extracted from the datasheet of IS42S16160J [:ref:`DS4 <reftable>`].

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

DDR2
----

The following requirements are extracted from the datasheet of IS43DR16320E [:ref:`DS5 <reftable>`].

.. requirement:: D_DDR2_01
   :rationale: This corresponds to an 5% precision arround 1.8V.
   :derivedfrom: U_MEMORY_02

   The VDD, VDDL and VDDQ supply voltages shall be within 1.7V and 1.9V with a current capacity of .

.. requirement:: D_DDR2_02
   :derivedfrom: U_MEMORY_02

   The VDD voltage ramp time shall not be greater than 200ms from when VDD ramps from 300mV to VDD min.

.. requirement:: D_DDR2_03
   :derivedfrom: U_MEMORY_02

   During the VDD voltage ramp, VDD and VDDQ shall not be futher apart than 300mV.

.. requirement:: D_DDR2_04
   :rationale: This corresponds to an 2% precision arround 0.5*VDDQ.
   :derivedfrom: U_MEMORY_02

   The VREF voltage shall be within 0.882V and 0.918V.

.. requirement:: D_DDR2_05
   :derivedfrom: U_MEMORY_02

   Peak to peak AC noise on VREF shall not exceed ±2% of VREF(dc).

.. requirement:: D_DDR2_06
   :rationale: VTT of the transmitting device must track VREF of the receiving device.
   :derivedfrom: U_MEMORY_02

   The VTT voltage shall be within VREF - 0.04 and VREF + 0.04.

.. requirement:: D_DDR2_07
   :derivedfrom: U_MEMORY_02

   The peak amplitude for the overshoot and undershoot area of the following pins shall be lower than 0.5V : Address, Control, Clock, Data, Strobe and Mask.

.. requirement:: D_DDR2_08
   :derivedfrom: U_MEMORY_02

   The amplitude area above VDD and below VSS of the following pins shall be lower than 1.33 V-ns : Address and Control.

.. requirement:: D_DDR2_09
   :derivedfrom: U_MEMORY_02

   The amplitude area above VDD and below VSS of the following pins shall be lower than 0.38 V-ns : Clock, Data, Strobe and Mask.

FPGA
----
