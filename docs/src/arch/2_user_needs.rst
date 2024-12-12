User needs
==========

Functions
---------

FPGA
^^^^

.. requirement:: U_FPGA_01
   :rationale: 85k LUTs with 365 I/Os. The speed grade of the part is not specified.

   The board shall include a Lattice ECP5 FPGA with reference LFE5U-85F-*BG756C.

Clock
^^^^^

.. requirement:: U_OSC_01
   :rationale: 30MHz LVCMOS, Enable/Disable on pin 1, 7.0x5.0mm package, 3.3VDC±5% supply, ±25ppm precision, -40 to +85°C temperature range.

   A 30 MHz reference oscillator shall be connected to one of the FPGA's global clock inputs, with reference XLH736030.000000I.

Memory
^^^^^^

Multiple volatile memories are included on the board with different technologies to provide the user with a memory controller development platform.

.. requirement:: U_MEMORY_01

   The board shall include a 256k x 16bits Asynchronous SRAM with reference IS61WV25616BLL up to -6 speed grade.

.. requirement:: U_MEMORY_02

   The board shall include a 16M x 16bits 256Mb Synchronous DRAM with reference IS42S16160J up to -6 speed grade.

.. requirement:: U_MEMORY_03
   :rationale: The -5B speed grade corresponds to DDR2-400B standard.

   The board shall include a 64M x 8bits 512Mb DDR2 Synchronous DRAM with reference IS43DR86400E up to -5B speed grade.

Flash
^^^^^

.. requirement:: U_FLASH_01
   :rationale: Only 32MBits are required to store the FPGA bitstream but the extra storage can be used by the user more easily than the eMMC. This reference supports optional programmable QSPI interface.

   The board shall include a 128Mbits NOR flash memory with reference W25Q128JVPIM to store the FPGA bitstream used in Quad-SPI configuration.

.. requirement:: U_FLASH_02

   The board shall include a 8GB eMMC flash memory with reference THGBMUG6C1LBAIL with High Speed DDR and HS200 support.

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

.. requirement:: U_CONNECTOR_01

   The board shall expose its various interfaces using a DDR4 SO-DIMM 260pin edge-card connector with the mapping specified in the following table.

.. image:: ../assets/io-pinout.svg
   :align: center
   :width: 50%

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
   * - SE[0-130]
     - I/O
     - Single-Ended general purpose input/output
   * - RD[0-64][P/N]
     - I
     - General purpose input differencial pair
   * - RTD[0-64][P/N]
     - I/O
     - General purpose input/output differencial pair
   * - RESET_I
     - I
     - Reset input
   * - VIN9_20
     - 
     - Main power input 9~20V
   * - unused
     - 
     - 
   * - GND
     - 
     - 

.. note:: Unused pins are left unconnected but reserved on the connector for future use.

Power
-----

.. requirement:: U_POWER_01

   The board shall include DC-DC converters converting the 9-15V input voltage to the appropriate voltages required by the board's components.

Mechanical
----------

.. requirement:: U_MECHANICAL_01
   :rationale: The board can be as tall as needed.

   The board shall match the DDR4 SO-DIMM edge-card horizontal dimensions and features.

.. requirement:: U_MECHANICAL_02

   The board shall include mounting holes around the FPGA to mount a heatsink.

