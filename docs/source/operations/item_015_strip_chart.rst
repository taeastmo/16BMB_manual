
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

3. Next to 'Log file', click :guilabel:`Browse...` and choose the name for the log file, 
   typically a new file in your own experiment data folder.

Logging can occur either automatically or manually. The program will automatically 
log a list of process variables (PV's) and data file names each time a new data file is saved (EDXD, or radiography). 
Alternatively, click :guilabel:`Record` at any time to log the then-current experimental parameters.
A time-stamped row of values will be appended to the log file each time.

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
