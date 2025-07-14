(F5) DDR2
=========

Functional description
----------------------

Design constraints
------------------

.. requirement:: D_MEMORY_03
   :rationale: The -5B speed grade corresponds to DDR2-400B standard.

   The board shall include a 64M x 8bits 512Mb DDR2 Synchronous DRAM with reference IS43DR86400E up to -5B speed grade.

The following requirements are extracted from the datasheet of IS43DR86400E [:ref:^DS5 <reftable>^].

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
     - All data, address and command signals must be followed within +- 50ps

   * - LC2
     - Intra-pair mismatch +- 2ps

   * - LC3
     - Inter-pair mismatch +- 5ps

   * - LC4
     - Intra-byte-group mismatch +- 10ps

CLK and DQS intra-pair and inter-pair mismatches are ignored as they are exactly length matched.

CLK, DQS, Data and DM signals are routed on the same layer (L6) and are length matched to 0.03mm (2.1ps<10ps).

Signals on L3/L6 shall be matched to 23.9150mm +- 5mm (35ps<50ps))

Signals on L8 shall be matched to 23.9150mm +- 7mm (35ps<50ps))
