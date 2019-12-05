# windowsStartStopLog
Python script that creates a logfile over windows start and log off time
This works on Windows 10 and Python version 3.7

1. Create a .bat file for the logStart.py script and place it in a folder that is included in the computer's PATH (environment variables).    Place a shortcut to it in the windows autostart folder.

2. Create a .bat file (e.g. logShutdown.bat) for the logShutdown.py script with the following code

   for %%i in (/Shutdown/*.py) do @python.exe C:/Shutdown/%%i

3. Create a folder on the C drive called Shutdown
4. Place the logShutdown.py file in the C:\Shutdown folder
5. Run gpedit.msc
6. Go to User Configuration -> Windows Settings -> Scripts -> Shutdown -> Properties and add the link to the logShutdown.bat file.

Make sure that the location of the .bat files are included in the PATH in the computer's environment variables.
