# Rest-Monitor
README.md

The files in this repository contain a proof of concept webserver monitor.  
This monitor does a GET call on each of the webservers as 
specified in the WebServerList.txt file.  It checks for errors and for the 
response time.  If a response takes too long (more than 2 seconds) or an
error is raised, an e-mail will be sent.  This monitor also logs info both
to the screen and to the RestMonitor.log file.  Configuration options
can be found in the RestMonitor.config file.  

The contained python script RestMonitor.py can be run from
the command line with:

python3 RestMonitor.py

This script is designed to send e-mail when there is an issue, however the
script must be modfied before that will work fully.  The function 
send_email_notification near line 133 in RestMonitor.py must be 
updated with the local smtp server information or a gmail username/cred 
must be supplied.

NOTE:  This script has only been tested on Windows using Python 3.6.0, but 
should run on Linux and/or earlier Python3 variants.  

Tom Sweeney, December 2016
tsweeney@alum.wpi.edu

