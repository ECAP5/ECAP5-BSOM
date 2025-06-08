Routing
=======

Stackup
-------

.. image:: ../assets/stackup.png
   :width: 70%
   :align: center

The stackup used is JLCPCB's JLC06121H-3313 1.2mm pcb stackup with a dielectric constant of 4.6.

.. flat-table:: Layer allocation
   :header-rows: 1
   :width: 100%

   * - Layer
     - Allocation

   * - Top layer L1
     - High-Speed signals

   * - Inner Layer L2
     - GND

   * - Inner Layer L3
     - Power

   * - Inner Layer L4
     - Power

   * - Inner Layer L5
     - GND

   * - Bottom layer L6
     - High-Speed signals

   * - Bottom layer L7
     - GND

   * - Bottom layer L8
     - High-Speed signals

Trace impedance
---------------

.. flat-table:: Net classes
   :header-rows: 1
   :width: 100%

   * - Impedance
     - Layer
     - Trace width
     - Differencial-pair spacing

   * - Single-ended 50ohms
     - L1/L6
     - 6.16mil (0,156464mm)
     - N/A

   * - Differencial 100ohm
     - L1/L6
     - 4.88mil (0,123952mm)
     - 8.0mil (0,2032mm)

   * - Single-ended 50ohms
     - L4
     - 5.29mil (0,134366mm)
     - N/A

   * - Differencial 100ohm
     - L4
     - 4.37mil (0,110998mm)
     - 8.0mil (0,2032mm)

.. note:: A 0.12mm single-ended trace will result in a 56ohm impedance on L1/L6 layers and a 53ohm impedance on L4.

.. note:: A 0.12mm differencial trace will result in a 101ohm impedance on L1/L6 layers and a 97ohm impedance on L4.

Signal propagation
------------------

The propagation speed is computed with the following formulas :

.. math::

   v_{\text{microstrip}} = \frac{c_{\text{vacuum}}}{\sqrt{Dk_{eff}}}

.. math::

   v_{\text{stripline}} = \frac{c_{\text{vacuum}}}{\sqrt{Dk}}

where Dkeff for a 0.12mm microstrip with a Dk of 4.6 is 2.87749 and the speed of light in vacuum is 299792458m/s.

.. flat-table:: Trace propagation on stackup layers
   :header-rows: 1
   :width: 100%
   
   * - Layer
     - Type
     - Propagation

   * - L1/L6
     - Single-Ended
     - 5.6583ps/mm

   * - L4
     - Single-Ended
     - 6.6713ps/mm

   * - L1/L6
     - Differencial
     - 

   * - L4
     - Differencial
     - 

.. note:: A maximum via delay of 20ps will be used.
