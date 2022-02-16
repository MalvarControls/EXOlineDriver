# Installation

Download the appropriate realease files:
- [EXOlineDriver-rt.jar](https://github.com/mc-simaodias/EXOlineDriver/releases) (Obligatory);
- [EXOlineDriver-wb.jar](https://github.com/mc-simaodias/EXOlineDriver/releases) (Obligatory);
- [EXOlineDriver-doc.jar](https://github.com/mc-simaodias/EXOlineDriver/releases) (Optional);

Paste them into the modules folder inside your Niagara installation directory ```C:\Niagara\Niagara-4.x.x.x\modules```.

# Change log

## Version 1.2.8 - Discovery fixes
Date: 16/02/2022

- Discovery of VPACs that specified 'AlignWithSegments' have been fixed. Depending on data types some addresses where being calculated incorrectly.

## Version 1.2.7 - Update Templates
Date: 14/02/2022

- Discovery of OIA28MIXW3BEM and OIA15MIXW3BEM points updated to reflect newer releases.

## Version 1.2.6 - Tempalte point discovery
Date: 09/02/2022

- Discovery of OIA28MIXW3BEM now works as intended. 

## Version 1.2.5 - Point descriptions
Date: 07/02/2022

- Proxy points now have a field to add a descriptive text. This is shown in the point manager and therefore exportable to the csv tables.

## Version 1.2.4 - Serial Communication
Date: 25/10/2021

- Fixed an issue that would prevent some RS-485 communications. If your project requires this type of communication it is required to perform an update to this version.

## Version: 1.2.3 - Compatibility issues
Date: 06/09/2021

- Fixed an issue that would make some control points not compatible across versions and not properly update.

## Version: 1.2.2 - Bug fixes

Date: 15/08/2021

- Fixed an issue where some invalid file extensions would not be ignored by the point discovery process;
- Now the EXOline device Manager will update appropriately the device information, without needing to open its configurations in a different tab;

## Version: 1.2.1 - Bug Fixes

Date: 28/09/2020

- Patched TCP/Serial device to accommodate for framework misbehaviour, which would make some requests drop;
- Fixed an issue where serial devices would sometimes not show up in the palette;
- Response max timeouts have been set to 5 seconds;

## Version: 1.0.0 - License Implementation

Date: 28/10/2019

- Driver now requires a valid license in order to function;
- TCP and Serial communications now have different instances of networks and devices in order to simplify complexity;
- Documentation updated;

Bug Fixes:

- Logs will now only be queried if the network and devices are not with fault states;

  

## Version: 0.3 - Logging Implementation

Date: 14/10/2019

- Added EXOline logs discovery;
- EXOoperator histories can be automatically created out of logs;
- Logs can be polled automatically or manually;
- Logs that have their histories enabled will be fully integrated with EXOoperator, allowing for graphical interfaces and exporting.
- Connection lost while getting records, will not erase logs from the controller;

Bug Fixes:

- EXOline messages that have '0x3E' byte somewhere in the middle of the message are not being cut short anymore;
- Variable discovery now take into consideration the number of pages of the Dpac;

## Version: 0.2.7 - Alarm Implementation

Date: 30/09/2019

- 0.2.7 open build released.

Date: 18/09/2019

- Added String exchange support to the driver;
- Texts.txe variables now show up during discovery actions;
- Variables are now displayed in alphabetical order inside it's DPac folder;
- Developer variables are now hidden;
- EXOline devices now have two different proxy folders one for points another for alarms;
- Added EXOline Alarm object;
- Added Alarm discovery;
- Updated documentation;

## Version: 0.2.6 - Template Revision

Date: 27/05/2019

- Corrected several variable data types to the correct ones on DI's and miscellaneous group.
- Message timeouts lowered to 200ms and ping retries lowered to 0;
- Ping rework: pings are only performed if any variable read failed for 10 times in a row or if the points folder are empty;

## Version: 0.2.5 - Ping Fixes

Date: 07/05/2019

- Device folder is now a legal parent to EXOline devices;
- Fixed an issue that pings were not being sent asynchronously;
- Added ping retries using the framework methods;
- Fixed an issue that wouldn't attempt the pings to re-ping up to 5 times on Serial connection;

## Version: 0.2.4 - Device Instantiation fixes

Date: 02/05/2019

- Adding a base EXOline device should now not throw an exception it if is not an IO template;
- IO15 and IO28 configurations were not being correctly set for Serial communication;
- Serial config only sets the default values if it is the first instantiation (after that it will use whatever values the user sets).
- First instantiation variable is now hidden from the user by default;

## Version: 0.2.3 - Point discover and pinging fixes

Date: 24/04/2019

- Polling and pinging should now not interfere with each other;
- Added the missing digital inputs to IO15;
- Fixed the DPE names of the IO15's and IO28's;
- Imported points now remain saved after a station restart;
- Discovery no longer gives a prompt when discovery command is issued;
- Devices are now set as disabled when added into a program.
