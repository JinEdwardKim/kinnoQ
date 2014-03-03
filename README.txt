Author: Edward Kim

27 FEB 2014
 - gps: gps module com
 - gis: comms between wps and server
 - nfc: nfc implementation
 - logger: logging into sqlite database
 - gui (use QT): qt user interface
 - sierra wireless 
 
 
 
 28 Feb 2014

 - create boggy gps to send to gis (done, sending location)
 - Logging in successful, receiving alarm msgs now
 
 Todo on Monday...
 - Timesheet (done)
 - nfc implementation? (using spi???)
 - trigger login and logout features
 - doesn't allow login process until valid gps
 - commandline user interface to trigger varius options? stdin is always monitoring the input for commands
 - 
 
 3 March 2014
 
 - Commandline implementation?
 
 - GPS program might needs to be completely separte from the main gis applicatino
 
 - nfc sl032? or 
 
 - gis, sqlite alarm
 
 TO DO NEXT!
 - alarm status check commandline (will return current strobe and siren status)
 - alarm acknowledging cmd (will set strobe and siren status to 0)
 - either new alarm or existing class_name increase its alarm status raises an alarm
 
 each time an alarm packet is received, need to check with existing data to make sure it works. 
 
 //int sqlite3CheckExistingAlarm(char* objName); //returns 0:false, 1:true


//if false, add record, if true, update or delete(if clear status)
//int sqlite3UpdateTableAdd(char* objName, int level); //updates table with new level (table is currentAlarm)
//currentAlarm table stores latest alarm status of alarm unique objName!
//sqlite3UpdateTableUpdate (Delete)