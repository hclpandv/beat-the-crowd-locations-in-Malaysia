# Find Windows Updates offline

https://ryanjan.uk/download-and-install-offline-windows-updates/

https://www.myerrorsandmysolutions.com/how-to-get-a-list-of-pending-windows-updates-of-a-server-with-no-internet-access-using-powershell/ 

https://github.com/wightsci/OfflineUpdateScanner

```powershell
Get-MSCatalogUpdate -Search "Cumulative Update for Windows 10 Version 20H2 for x64-based Systems" | `
?{($_.products -like "*Windows 10, version 1903*") -and ($_.title -notlike "*Preview*") }

Get-MSCatalogUpdate -Search "Cumulative Update for Windows Server 2016 for x64-based Systems" | `
?{($_.products -like "*Windows Server 2016*") -and ($_.title -notlike "*Preview*") }

```
