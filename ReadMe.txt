###############################ReadME###############################
### Example on how to use the hpl2netCDF client ###

1.	Go to the directory where the package is located and install the client via 'pip install .'
	If installation was not successful, please contact Markus.Kayser@dwd.de
2.	Usage:
	After the successful installation the client can be used through parsing the following commands:
	You need to specify a valid date with either '-d' or '-date' and a command to execute with '-c' or '-cmd'.
	The following commands are valid:
		- 'hpl_l1' creates a daily netCDF file of lvl1 .hpl-files.
		- 'l1_l2' processes a daily lvl1 netCDF file according to the VAD retrieval described in Päschke et al. [2015].
		- 'hpl_l1_l2' creates daily lvl1 and lvl2 netCDF files from .hpl-files.
        Note: In case of lvl2 processing you can add ...'wql' to the command to create quicklooks.
	You have to specify a custom configuration file in order for the routines to locate .hpl-files and give directories of lvl1 and lvl2 netCDFs as well as of quicklooks.
    The routines will create a data path corresponding to YYYY/YYYYMM.
	This is done with the command '-u' or '-url', followed by the path to the configuration file, including the file name.
	Examples:
		using custom configuration file:
		'hpl2netCDF-client -u "configuration file" -d "specify date as YYYY-MM-DD" -c "cmd"'