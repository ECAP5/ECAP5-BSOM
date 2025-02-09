(F3) SRAM
=========

Functional description
----------------------

The SRAM sub-circuit is in charge of providing the user with 4MiB of Asynchronous SRAM.

Design constraints
------------------

.. requirement:: D_MEMORY_01

   The board shall include a 256k x 16bits Asynchronous SRAM with reference IS61WV25616BLL up to -8 speed grade.

The following requirements are extracted from the datasheet of IS61WV25616BLL [:ref:^DS3 <reftable>^].

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


Circuit diagram
---------------

Design calculations
-------------------

Considering a read access time of 8ns, for one of the address or IO signals, the Data Transfer Rate is :math:`1 / 8\text{ns} = 125\text{Mbps}`.

The highest signal frequency content is given as :

.. math::

  F_m = 2.5 * \text{DTR} = 2.5 * 125 * 10^6 = 312.5\text{MHz}

Using Kicad's wavelength calculator tool with :math:`E_r = 4.04` (FR4 370HR), we get a wavelength of :math:`\simeq 45\text{cm}`.

The address and IO signals are therefore considered low-speed as long as the traces are less than 45cm.

.. todo:: Check with the final material

Simulation results
------------------
