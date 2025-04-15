Routing
=======

Stackup
-------

.. image:: ../assets/stackup.png
   :width: 70%
   :align: center

The stackup used is JLCPCB's JLC06121H-3313 1.2mm pcb stackup.

.. flat-table:: Layer allocation
   :header-rows: 1
   :width: 100%

   * - Layer
     - Allocation

   * - Top layer
     - High-Speed signals

   * - Inner Layer L2
     - GND

   * - Inner Layer L3
     - Power

   * - Inner Layer L4
     - Low-Speed signals

   * - Inner Layer L5
     - GND

   * - Bottom layer
     - High-Speed signals

Net classes
-----------

.. note:: Controlled impedance traces shall be routed on outer layers.

.. flat-table:: Net classes
   :header-rows: 1
   :width: 100%

   * - Type
     - Trace width
     - Trace spacing
     - Differencial-pair spacing

   * - 50ohm impedance classes
     - 6.16mil
     - 3*6.16mil
     - 

   * - 100ohm impedance classes
     - 4.88mil
     - 3*4.88mil
     - 8.0mil



