# Ghosts automation

## Preparing Windows Workstations:

Use a Windows 10 or Windows 11 machine

### Enabling SSH server on Windows

```powershell
Add-WindowsFeature -Name OpenSSH-Server
Start-Service sshd
Set-Service -Name sshd -StartupType 'Automatic'
New-NetFirewallRule -Name sshd -DisplayName 'OpenSSH Server (sshd)' -Enabled True -Direction Inbound -Protocol TCP -Action Allow -LocalPort 22
```

