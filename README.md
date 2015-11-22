#WMIOps

WMMIOps is a powershell script that uses WMI to perform a variety of actions on hosts, local or remote, within
a Windows environment.  It's designed primarily for use on penetration tests or red team engagements.

This is my first PowerShell script, so I am sure there's things that could have been done better.  Please submit
a request for anything that could be made more efficient and I'd be happy to look at it, and learn from it :).

Developed by [@christruncer](https://twitter.com/christruncer)

Thanks to:
    [@mattifestation](https://twitter.com/mattifestation) for your major work in this area (Posh and WMI), 
    [@obscuresec](https://twitter.com/obscuresec), [@enigma0x3](https://twitter.com/enigma0x3), [@424f424f](https://twitter.com/424f424f), [@xorrior](https://twitter.com/xorrior), and [@sixdub](https://twitter.com/sixdub) for having already solved a lot of PowerShell problems and publishing your code to let me, and others, learn from it
    [@harmj0y](https://twitter.com/harmj0y) - for helping to mentor me from the beginning
    [@evan_Pena2003](https://twitter.com/evan_pena2003) - For your help with code reviews and teaching me what to look into and learn


## WMIOps Functions:
    Invoke-ExecCommandWMI               -   Executes a user specified command on the target machine
    Invoke-KillProcessWMI               -   Kills a process (via process name or ID) on the target machine
    Get-RunningProcessesWMI             -   Returns all running processes from the target machine
    Get-ProcessOwnersWMI                -   Returns all accounts which have active processes on the target system
    Find-ActiveUsersWMI                 -   Checks if a user is active at the desktop on the target machine (or if away from their machine)
    Invoke-CreateShareandExecute        -   Creates a share, copies file into it, uses WMI to invoke the script on the target system, from the local system, via UNC path
    Invoke-RemoteScriptWithOutput       -   Executes a powershell script in memory on the target host via WMI and returns the output
    Find-UserSpecifiedFileWMI           -   Search for a file (wildcard supported) on a target system
    Invoke-FileTransferOverWMI          -   Uploads or Downloads files to/from the target machine over WMI