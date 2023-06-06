# PowerShell Cheat Sheet

## Find local resources

Display path to `powershell.exe`
```powershell
(Get-Process -Id $pid).Path
```

Display path to profile location
```powershell
$profile
```

Get powershell history path
```powershell
(Get-PSReadlineOption).HistorySavePath
```

Get current directory location
```powershell
Get-Location
```

## Output versions

Display version table
```powershell
$PSVersionTable
```

Display version
```powershell
$PSVersionTable.PSVersion
```

## Environment variables

Display path
```powershell
$env:path
```

Update env variables
```powershell
$refreshenv
```

## New files and directories

Create new directory
```powershell
New-Item -Path 'C:\temp\New Folder' -ItemType Directory
```

Create new file
```powershell
New-Item -Path 'C:\temp\New Folder\file.txt' -ItemType File
```

## Operation details

List all available commands
```powershell
Get-Command
```

Get help with other command (Write-Host is an example parameter)
```powershell
Get-Help Write-Host
```

Display running processes
```powershell
Get-Process
```

Get event logs (shown with example parameters)
```powershell
Get-EventLog -LogName System -After “09/28/2015” -Before “09/29/2015” | Where-Object {$_.EntryType -like ‘Error’ -Or $_.EntryType -like ‘Warning’} | Sort-Object Source
```

Display list of installable services
```powershell
Get-Service
```

## System commands

Shut down computer
```powershell
Stop-Computer
```

Restart operating system
```powershell
Restart-Computer
```

Force immediate restart
```powershell
Restart-Computer -Force
```

## Customize output color for Git

### Option 1

Add the following snippet to your `.gitconfig` file

```
[color]
   ui = true
[color "status"]
   changed = red bold
   untracked = red bold
   added = green bold
```

### Option 2

```powershell
git config color-to-update "foreground-color background-color attribute"
```

Usage example

```powershell
git config --global color.status.changed "cyan normal bold"
```
