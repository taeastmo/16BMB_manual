.. _hpMCA:

hpMCA
=====



GUI basics
----------

.. figure:: /images/hpmca/start_file_loaded.png
   :alt: start_file_loaded
   :scale: 50 %
   :align: center

Left panel (from top to bottom):

- :ref:`Acquisition <acquisition>`
- :ref:`Elapsed time  <elapsed_time>`
- :ref:`Save data file  <save_data_file>`
- :ref:`File saving options <file_save_options>`
- :ref:`Regions of interest <rois>`
- :ref:`Fluorescence markers <fluorescence>`
- :ref:`Vertical scale <v_scale>`
- :ref:`Horizontal scale <h_scale>`

The plot area supports the following mouse commands:

- *Left Click:*
    Move the vertical line cursor to the current mouse position.   

- *Left Drag:*
    Zoom-in to the selected area.

- *Right Click:*
    Zoom out.

- *Mouse Wheel:*
    Zoom in and zoom out centered around the current mouse position.

Bottom panel: Energy and Counts information corresponting to location selected by the cursor

Menu bar: 

* File
   * Open file
   * Open detector
   * Overlay
   * Save as
   * Export pattern
   * Environment
   * Multiple spectra

* Control
   * Calibrate Energy
   * Calibrate 2-theta
   * Set 2-theta
   * Set wavelength
   * Presets

* Display
   * Phase
   * Fluorescence
   * Retions of interest
   * Lattice refinement
   * Colors options
   * ROI options

.. _acquisition:

Acquisition
-----------

- To start data collection, press ‘Erase’ and then ‘On’ in ‘Acquisition’ panel.
- To stop data collection and to save, press ‘Off’ in ‘Acquisition’.

.. _elapsed_time:

Elapsed time 
------------
Elapsed time section

.. _save_data_file:

Save data file
--------------
Save data file section

.. _file_save_options:

File saving options
-------------------

File saving options section



.. _rois:

Regions of Interest (ROI)
-------------------------
There are two methods to add an ROI.

(1)	:ref:`Manual selection of ROI. <manual_roi>`
(2)	:ref:`Make ROI on all peaks for a crystal by using the JCPDS data. <jcpds_roi>`

.. _manual_roi: 

    (1)	**Manual selection of ROI**

        #. Select center of region of interest by moving cursor to that position (Left-click with mouse).
        #. Click, ‘Add’ button in ‘ROIs’ panel. The button will now read ‘Set’.
        #. Drag left and right extends of the ROI to appropriate positions.

        .. figure:: /images/hpmca/roi_set.png
           :alt: hpmca_roi_set
           :scale: 45 %
           :align: center
           
        4. Then, click ‘Set’ button in ‘ROIs’ panel. The ROI area should now be a different color (default – blue).
        #. Currently selected ROI is indicated by a red cursor above it.
        #. The Centroid of the selected ROI is displayed in top-middle of the plot.
        #. Different ROI can be selected by ‘<’ and ‘>’ buttons in the ROI panel.
        #. More information about the ROIs can be displayed in the ‘ROIs control’ by selecting menu: Display/ROIs.
        #. You can change the name of any ROI by double-clicking and typing a new name in the name column.
        #. Peak fit can be displayed by clicking ‘Show fit’ button in ROIs control window.

    .. figure:: /images/hpmca/rois.png
       :alt: rois
       :scale: 80 %
       :align: center

    .. figure:: /images/hpmca/hpmca_roi_control.png
       :alt: hpmca_roi_control
       :scale: 70 %
       :align: center

.. _jcpds_roi: 

    (2)	**Make ROIs on all peaks for a crystal by using JCPDS phase**

        #. Open ‘Phase control’ window from menu Display -> Phase
        
        .. figure:: /images/hpmca/phase.png
           :alt: phase
           :scale: 80 %
           :align: center 

        2. Select material by opening a jcpds file.
        #. Check if 2𝜽 angle is correct, adjust if needed.
        #. Lines, which indicate positions of the peaks of the material, appear below EDXD data.

        .. figure:: /images/hpmca/hpmca_phase_lines.png
           :alt: hpmca_phase_lines
           :scale: 80 %
           :align: center
        
        5. The positions of peaks lines can be shifted by changing ‘P (GPa)’, or ‘T (K)’.
        
        #. Then, click ‘Add ROIS’ in ‘Phase control’ window to add ROIs for all peaks.

To erase a ROI, please click ‘Delete’ after selection of the ROI.
To erase all ROIs, please click ‘Clear All’.

.. _fluorescence:

Fluorescence markers
--------------------  

By typing in an element, hpMCA shows K and/or L shell emission lines positions.

.. _v_scale:

Vertical scale
-------------------

Vertical scale section

.. _h_scale:

Horizontal scale
----------------

Horizontal scale section

Energy calibration
------------------
Beamline scientist does energy calibration of the germanium solid state detector by using Fluorescence lines of silver at 22.104 keV (K𝜶) and 24.942 keV (K𝜶1), and gammas from 109Cd (88.04 keV) and 57Co (122.10  keV) at the beginning of each beamtime cycle.  Parameters of energy calibration (Energy=CAL_OFFSET+CAL_Slope×Channel) can be found in the header of the EDXD data file.

.. figure:: /images/hpmca/hpmca_file_header.png
   :alt: hpmca_file_header
   :scale: 70 %
   :align: center

2𝜽 angle calibration
--------------------
Beamline scientist does 2𝜽 angle calibration at 7°, 15°, 23°, and 31° using unit-cell volume of Au, and make linear equation to calculate 2𝜽 angle.

The following is the procedure for 2𝜽 angle calibration:

- Collect Au EDXD pattern.
- Make ROIs for all Au peaks using JCPDS data at 0 GPa (cf. page 14).
- Select Control -> Calibrate 2theta… on Menu bar.
- Please remove weak or overlapping peaks by selecting ‘No’ in the second column ‘Use?’.

.. Note:: Because the MCA does not have background subtraction feature, background slope at low energy (<~25 keV) probably due to absorption influences on determining peak position. It is better not to use low energy data for 2𝜽 angle calibration. Typically, at 2𝜽 of ~15 °, the first and second peaks show marked deviation from other peaks.

- Click ‘Compute 2𝜽’.
- 2𝜽 value appears in the ‘2𝜽’ box.
- Then, please click OK to apply the 2𝜽 calibration.

.. figure:: /images/hpmca/hpmca_2theta_calibration.png
   :alt: hpmca_2theta_calibration
   :scale: 70 %
   :align: center

.. note:: The 2𝜽 calibration result is also saved in the header of the data file.

