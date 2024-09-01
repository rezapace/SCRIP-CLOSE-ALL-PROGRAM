# SCRIP-CLOSE-ALL-PROGRAM

## Description

This PowerShell script retrieves a list of all running processes on your computer, checks if they have a window title (`mainwindowtitle`), and ensures they are not PowerShell itself. If these conditions are met, the `stop-process` command is used to close those programs.

## Key Features

- Retrieves all running processes.
- Filters out processes without a window title.
- Excludes PowerShell from being terminated.
- Closes all qualifying programs.

## How to Use

1. **Download the Script**: Download the `script-close-all-program.ps1` file.
2. **Run the Script**: Double-click the downloaded file to execute it.
3. **Effect**: The script will close all running programs on your computer, except for PowerShell.

## Important Notes

- **Save Your Work**: Ensure you save all your work and close any programs you want to keep open before running this script.
- **Data Loss Warning**: Any unsaved data or improperly saved work will be lost if the program is closed by this script.

## Example Command

```powershell
(get-process | ? { $_.mainwindowtitle -ne "" -and $_.processname -ne "powershell" } )| stop-process
```

This command retrieves all processes with a window title, excludes PowerShell, and stops the remaining processes.


