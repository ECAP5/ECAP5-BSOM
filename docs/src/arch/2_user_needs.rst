User needs
==========

Functions
---------

FPGA
^^^^

.. requirement:: U_FPGA_01
   :rationale: 85k LUTs with 2.5Gb/s transceivers with 365 I/Os. The speed grade of the part is not specified.

   The board shall include a Lattice ECP5 FPGA with reference LFE5UM-85F-*BG756C.

Memory
^^^^^^

Multiple volatile memories are included on the board with different technologies to provide the user with a memory controller development platform.

.. requirement:: U_MEMORY_01

   The board shall include a 256k x 16bits Asynchronous SRAM with reference IS61WV25616BLL up to -8 speed grade.

.. requirement:: U_MEMORY_02

   The board shall include a 8M x 32bits 256Mb Synchronous DRAM with reference IS42S32800J up to -6 speed grade.

.. requirement:: U_MEMORY_03
   :rationale: The -5B speed grade corresponds to DDR2-400B standard.

   The board shall include a 32M x 16bits 512Mb DDR2 Synchronous DRAM with reference IS43DR16320E up to -5B speed grade.

.. todo:: Add DDR3 if enough pins

Flash
^^^^^

.. requirement:: U_FLASH_01
   :rationale: Only 32MBits are required to store the FPGA bitstream but the extra storage can be used by the user more easily than the eMMC. This reference supports optional programmable QSPI interface.

   The board shall include a 128Mbits NOR flash memory with reference W25Q128JVPIM to store the FPGA bitstream used in Quad-SPI configuration.

.. requirement:: U_FLASH_02

   The board shall include a 16GB eMMC flash memory with reference KLMAG1JETD-B041.

Miscellaneous
^^^^^^^^^^^^^

.. requirement:: U_BUTTON_01

   The board shall include a reset button which shall reset the FPGA.

.. requirement:: U_BUTTON_02

   The board shall include a user button which shall be wired to the FPGA.

.. requirement:: U_LED_01

   The board shall include a status LED which shall indicicate the status of the FPGA.

.. requirement:: U_LED_02

   The board shall include a user LED which shall be driven by the FPGA.

Interfaces
----------

.. todo:: 4x 2.5Gb/s SERDES (General purpose)

.. requirement:: U_CONNECTOR_01

   The board shall expose its various interfaces using a DDR4 SO-DIMM 260pin edge-card connector with the mapping specified in the following table.

.. csv-table:: SO-DIMM IO Connector Pinout
  :header-rows: 1
  :file: ../assets/io-pinout.csv
  :delim: ;
  :width: 100%

.. list-table:: SO-DIMM IO Connector Signal Description
   :header-rows: 1
   :width: 100%

   * - Name
     - Type
     - Description

   * - JTAG_TCK
     - I
     - JTAG clock input
   * - JTAG_TDI
     - I
     - JTAG data input
   * - JTAG_TDO
     - O
     - JTAG data output
   * - JTAG_TMS
     - I
     - JTAG test mode select input

   * - VIN9_20
     - 
     - Main power input 9~20V

Power
-----

.. requirement:: U_POWER_01

   The board shall include DC-DC converters converting the 9-20V input voltage to the appropriate voltages required by the board's components.

Mechanical
----------

.. requirement:: U_MECHANICAL_01
   :rationale: The board can be as tall as needed.

   The board shall match the DDR4 SO-DIMM edge-card horizontal dimensions and features.

.. requirement:: U_MECHANICAL_02

   The board shall include mounting holes around the FPGA to mount a heatsink.

