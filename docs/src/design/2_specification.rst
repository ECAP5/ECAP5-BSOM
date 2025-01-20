Specification
=============

.. requirement:: U_FPGA_01
   :rationale: 85k LUTs with 365 I/Os. The speed grade of the part is not specified.

   The board shall include a Lattice ECP5 FPGA with reference LFE5U-85F-*BG756C.

.. requirement:: U_CLOCK_01

   The board shall include a 40MHz clock generator which shall be connected to one of the FPGA's global input clock pins.

.. requirement:: U_MEMORY_01

   The board shall include a 16-bit SRAM memory IC.

.. requirement:: U_MEMORY_02

   The board shall include a 16-bit SDRAM memory IC.

.. requirement:: U_MEMORY_03

   The board shall include a 8-bit DDR2 memory IC.

.. note:: Multiple different memory technologies are integrated into the board to allow experimenting with memory controller development.

.. requirement:: U_STORAGE_01
   :rationale: 32Mb of storage is enough to store the FPGA bitstream but a bigger IC can be used to store user data.

   The board shall include a Quad-SPI Flash memory IC with at least 32Mb of storage which shall be connected to the FPGA sysConfig pins.

.. requirement:: U_STORAGE_02

   The board shall include an eMMC flash memory IC with HS200 support.

.. requirement:: U_CONNECTOR_01

   The board shall expose its various interfaces using a DDR4 SO-DIMM 260pin edge-card connector with the following pinout

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

.. requirement:: U_POWER_01

   The board shall be powered by the 9-15V power inputs from the IO connector.

.. requirement:: U_MECHANICAL_01
   :rationale: The board can be as tall as needed.

   The board shall match the DDR4 SO-DIMM edge-card horizontal dimensions and features.

.. requirement:: U_MECHANICAL_02

   The board shall include mounting holes around the FPGA to mount a heatsink.

.. requirement:: U_LED_01

   The board shall include a status LED which shall indicicate the status of the FPGA.

.. requirement:: U_LED_02

   The board shall include a user LED which shall be driven by the FPGA.

