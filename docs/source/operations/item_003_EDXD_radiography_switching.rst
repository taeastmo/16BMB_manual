EDXD and radiography mode switching
-----------------------------------
There are currently three modes of operation:

1. EDXD with direct (collimated) beam
2. EDXD with condensed beam 
3. Radiography imaging with direct beam

Direct beam mode delivers a collimated beam for EDXD diffraction measurements. The size of the beam can be adjusted by varying the sizes of the incident slits, with a typical size being 100 (H) x 300 (V) microns. If the user desires higher flux, the condensed beam mode can be used to focus 1 mm of beam in the horizontal direction down to 20 microns (typical vertical size remains at 300 microns). This provides roughly 7.5x the on-sample flux as compared to using the collimated beam. Finally, radiography measurements can be acheived with a large collimated beam, typically 1 x 1 mm. This page provides instructions on setting up each mode so that during the experiment, users can switch between them with the push of a button.





| Setup of slits and filter for EDXD and radiography measurement.
| Open :guilabel:`Slits/Filter Setup` on the PEC user interface.

.. figure:: /images/operation/slits_filter_interface.png
   :alt: slits_filter_interface
   :width: 500px
   :align: center

Input slit sizes and filter setup values in the 'Preset Position' window. 

.. warning:: Please do not change other parameters (e.g., Tip X, Y, Z, and so on).

   

Setup 1 is for EDXD measurements and setup 2 is for radiography measurement. Filter value 
is typically 0 (no filter) for EDXD measurement and -45 (100 μm molybdenum) for 
radiography measurement. Please close the window after completion.
'1-st Hsize', '1-st Vsize', '2-nd Hsize', '2-nd Vsize', 'Filter' setups change 
simultaneously by clicking :guilabel:`Slit for EDXD` (EDXD) or :guilabel:`For Camera` (radiography).

.. figure:: /images/operation/slit_mode_switch.png
   :alt: slit_mode_switch
   :width: 720px
   :align: center
