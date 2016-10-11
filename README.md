# PowerShell-d00mReport
PowerShell module that will help create HTML reports on a variety of things. When set up as a Windows Scheduled Task, these functions can provide logging and documentation possibilities because honestly, who likes documenting things.

## System Hardware
This is a catch-all report that uses CIM to query...
- Win32_BaseBoard
- Win32_Bios
- Win32_CdRomDrive
- Win32_ComputerSystem
- Win32_DiskDrive
- Win32_LogicalDisk
- Win32_NetworkAdapter
- Win32_NetworkAdapterConfiguration
- Win32_OperatingSystem
- Win32_PhysicalMemory
- WMIMonitorID
- Win32_Processor
And writes it all to an awesome looking HTML report to wow your friends!

## Installed Software
Using the Registry, this will create an HTML report detailing what information it can about installed software. __Most__ of the time there isn't any information in the registry about a piece of installed software, so your mileage may vary. Handy for taking stock of what a particular system is set up to do, however.

## Services
Uses the PowerShell Get-Process cmdlet to get various properties of a system's services and creates a fancy HTML report

## Disk Space
Uses CIM to query Win32_LogicalDisk to create a fancy HTML report that lists systems disk space space utilization

## Architecture
Uses CIM to query Win32_Processor and Win32_OperatingSystem to check for 32- or 64-bitness of a computer and host operating system

## Event Logs
Uses the PowerShell cmdlet Get-EventLog to get __all__ the event logs on a system and all of the Error, Warning, or FailureAudit event types in the last 24 hours

## WinSat Score
Uses the WinSat.exe prepop command line utility to create an HTML report outlining a systems Windows Performance Score

## Monitors
Uses CIM to query root/WMI/WmiMonitorID properties of all monitiors associated with a computer. Not particularly useful for Windows Server Core installations or VMs, but handy for inventorying a bunch of clients!
