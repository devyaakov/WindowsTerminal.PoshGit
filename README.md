# Configurar Posh-Git para Windows Terminal

Los siguientes comandos son para dar permisos de ejecuciones de scripts en que caso que lo solicite *PowerShell*

```PowerShell
Get-ExecutionPolicy
Set-ExecutionPolicy Unrestricted
Set-ExecutionPolicy Restricted
```

Para instalarlo abrimos una línea de comandos de *PowerShell* (vale con cualquiera de los dos: el "clásico" o el "Core"):

```PowerShell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Paradox
```

Se crea un archivo en la siguiente ruta
__*C:\Users\<Usuario>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1*__
```PowerShell
notepad.exe $profile
```

Agregandole las siguientes lineas

```ps1
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Paradox
```
