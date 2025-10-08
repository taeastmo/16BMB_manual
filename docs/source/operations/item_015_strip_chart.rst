
Logging data with Strip Chart
--------------------

The strip chart software can be used to continuously monitor various PVs (e.g., pressure, temperature, heater power, etc.).

1. Open 'Strip Chart' from desktop shortcut.

   .. figure:: /images/strip_chart/strip_chart_initialized.png
      :alt: strip_chart_initialized
      :width: 550px
      :align: center

2. From the 'File' menu, select 'Open' and then select the folder 'stipChart-setup-files.' This will show a list of configuration files that tell the Strip Chart which PVs to monitor. The beamline staff can help you customize a file if needed. For basic pressure and temperature logging, select 'Pressure-temperature-log.xml.'

   .. figure:: /images/strip_chart/strip_chart_setup_files.png
      :alt: strip_chart_setup_files
      :width: 450px
      :align: center

3. Next, navigate to the directory where you want to save your strip chart data and create a blank text file.

   .. figure:: /images/strip_chart/blank_strip_chart.png
      :alt: blank_strip_chart
      :width: 550px
      :align: center

4. Navigate back to the Strip Chart interface. From the menu, select 'Save Data -> Start' and then navigate to the blank .txt file you just created. Select the file and click 'Save.' This will create an additional .txt file to which the strip chart software will write the monitored PVs. 

   .. figure:: /images/strip_chart/saving_strip_chart.png
      :alt: saving_strip_chart
      :width: 550px
      :align: center


**LogBook** allows recording any process variable (PV); however 
a pre-defined list of PV's is stored in setup ``*.env`` file in the program's ``resources`` directory.

The following default PV's will be logged:

.. csv-table:: LogBook PV's
   :header: "Description", "PV"
   :widths: 50, 100
   :file: tables/table7_logbook_settings.csv

.. note:: Text entered into the 'Note' field will also be logged each time. 
   The Note text can be changed by the user at any time and can be up to 80 characters long.

.. figure:: /images/logbook/record.png
   :alt: log_book_new
   :width: 500px
   :align: center
