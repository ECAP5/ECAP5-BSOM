Introduction
============

Purpose
-------

This documents aims at defining the functional requirements for ECAP5-BSOM as well as documenting the design process.

Product Scope
-------------

ECAP5-BSOM is a System-On-Module board which shall provide ECAP5 with a general-purpose FPGA platform including integrated memory, flash storage and high-speed interfaces.

Intended Use
-------------------------

ECAP5-BSOM is targetted at ECAP5 

Conventions
-----------

Requirement format
^^^^^^^^^^^^^^^^^^

This document details requirements with the following format :

.. list-table:: Sample requirement
  :width: 100%
  :widths: 10 90

  * - **ID**
    - Requirement_ID

  * - **Description**
    - Requirement description

  * - **Rationale**
    - Requirement rationale

  * - **DerivedFrom**
    - Other_Requirement_ID

with requirement IDs having the following format :

  * ``U_*``: User requirements
  * ``D_*``: Design requirements

Definitions and Abbreviations
-----------------------------

.. todo:: Update the ref table

.. _reftable:

References
----------

.. list-table::
  :header-rows: 1
  :widths: 10 20 15 55
  :width: 100%
  
  * - Reference
    - Date
    - Version
    - Title

  * - DS1
    - March 27, 2018
    - Revision F
    - W25Q128JV 3V 128M-Bit Serial Flash Memory with Dual/Quad SPI

  * - DS2
    - October 1, 2019
    - Revision 2.0
    - THGBMJG6C1LBAIL e-MMC Module

  * - DS3
    - July 20, 2022
    - Revision H2
    - IS61WV25616BLL 256K x 16 High Speed Asynchronous CMOS Static RAM 

  * - DS4
    - September 16, 2020
    - Revision C4
    - IS42S16160J 16Meg x16 256Mb Synchronous DRAM

  * - DS5
    - December 11, 2017
    - Revision B
    - IS43DR16320E 32Mx16 DDR2 DRAM

  * - DS6
    - September 21, 2023
    - N/A
    - Plastic Package Ultra Miniature Pure Silicon Clock Oscillators

  * - AN1
    - May, 2023
    - 1.4
    - FPGA-TN-02210 Power Consumption and Management for ECP5 and ECP5-5G Devices
