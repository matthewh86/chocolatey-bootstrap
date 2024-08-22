# Chocolatey bootstrap

Launch as administrator
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
Invoke-WebRequest "https://raw.githubusercontent.com/matthewh86/chocolatey-boostrap/master/packages.config" -OutFile "packages.config"
choco install packages.config
```
