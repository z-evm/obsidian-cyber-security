## 🔹 Basics

##### Print text
```
Write-Output "Hello, PowerShell!"
Write-Host "Visible output"
```
##### Variables
```
$myVar = "Hello"
$num = 42
```
##### Data types
```
[int]$x = 5
[string]$name = "Zac"
$array = @(1, 2, 3)
$hash = @{Key="Value"; Another="Thing"}
```
##### Comments
```
# Single line comment
<#
Multiline
comment
#>
```

---
## 🔹 Control Flow
##### If / Else
```
if ($x -gt 10) { "Big" } else { "Small" }
```
##### Switch
```
switch ($num) {
  1 { "One"; break }
  2 { "Two"; break }
  default { "Unknown" }
}
```
##### Loops
```
for ($i = 0; $i -lt 5; $i++) { $i }
foreach ($item in $array) { $item }
while ($x -lt 10) { $x++ }
```

---
## 🔹 Functions

```
function Say-Hello {
  param($Name)
  "Hello, $Name!"
}

Say-Hello -Name "Zac"
```

---
## 🔹 Common Cmdlets

##### File & Directory
```
Get-ChildItem         # ls/dir
Set-Location C:\      # cd
Get-Content file.txt  # cat
Copy-Item a.txt b.txt # cp
Move-Item a.txt b.txt # mv
Remove-Item file.txt  # rm
New-Item -ItemType File -Name "new.txt"
New-Item -ItemType Directory -Name "stuff"
```
##### System Info
```
Get-Process
Get-Service
Get-EventLog -LogName System -Newest 10
Get-HotFix             # Installed updates
```
##### Networking
```
Test-Connection google.com
Resolve-DnsName github.com
Get-NetIPAddress
Get-NetTCPConnection   # Like netstat
```

---
## 🔹 Scripting & Automation

##### Run a script
```
.\script.ps1
```
##### Scheduled task example
```
Register-ScheduledTask -Action (New-ScheduledTaskAction -Execute "notepad.exe") `
  -Trigger (New-ScheduledTaskTrigger -AtLogOn) `
  -TaskName "OpenNotepadAtLogin" -Description "Opens Notepad"
```
##### Run PowerShell as Admin
```
Start-Process powershell -Verb runAs
```

---
## 🔹 Piping & Filtering
```
Get-Process | Where-Object {$_.CPU -gt 100}
Get-Service | Sort-Object Status | Format-Table -AutoSize
```
---
## 🔹 Useful One-Liners

##### Get IP address
```
(Get-NetIPAddress -AddressFamily IPv4 -InterfaceAlias "Wi-Fi").IPAddress
```

##### Kill a process
```
Stop-Process -Name notepad
```

##### List startup programs
```
Get-CimInstance -ClassName Win32_StartupCommand
```

##### Search files for string
```
Get-ChildItem -Recurse -Filter *.ps1 | Select-String -Pattern "Get-Process"
```

---

## 🔹 Security & Permissions
##### Execution policy
```
Get-ExecutionPolicy
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
##### Get local users
```
Get-LocalUser
```
##### Check if running as Admin
```
if (-not ([Security.Principal.WindowsPrincipal] `
  [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole(`
  [Security.Principal.WindowsBuiltInRole]::Administrator)) {
  "You’re not admin, my dude."
}
```

---
## 🔹 Modules & Help

```
Get-Command              # All available commands
Get-Command Get-*        # Commands starting with Get-
Get-Help Get-Process     # Show help
Update-Help              # Download updated help
Import-Module NetSecurity
```

---

## 🔹 Dev & Debugging

##### Try/Catch block
```
try {
  1 / 0
} catch {
  "Error: $_"
}
```
##### Measure execution time
```
Measure-Command { Get-Process }
```
##### Environment variables
```
$env:Path
$env:USERNAME
```

---

## 🔹 .NET Interop
```
Add-Type -AssemblyName System.Windows.Forms
[System.Windows.Forms.MessageBox]::Show("PowerShell FTW!")

[datetime]::Now
[Math]::Sqrt(144)
```

---

## 🔹 WSL + PowerShell

##### Run Linux command from PowerShell
```
wsl ls -la
wsl sudo apt update
```

---

## 🧩 Pro Tips

- Use `PSReadLine` for syntax highlighting and command history (enabled by default).
- Use **VS Code** with the **PowerShell extension** for the best editing/debugging experience.
- `Ctrl + J` in VS Code brings up PowerShell snippets.
- Dot-source reusable snippets: `. .\mysnippets.ps1`
- PowerShell 7+ is cross-platform and faster than Windows PowerShell 5.1.

---
