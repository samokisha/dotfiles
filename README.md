# dotfiles

## Windows PowerShell
### Install [scoop](https://scoop.sh/)
```powershell
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
```

### Install [Starship](https://starship.rs/) via `scoop`
```powershell
scoop install starship
```

### Create `PowerShell` profile and add init `Starship` line to end of file
```powershell
New-Item -Type File -Path $PROFILE -Force
echo "Invoke-Expression (&starship init powershell)" >> $PROFILE
```

### Configure `Starship`
Create config file
```powershell
New-Item -Type File -Path ~/.config/starship.toml -Force
```

Replace content with [starship.toml](.config/starship.toml)