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
