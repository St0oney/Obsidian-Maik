# Get Host Details

-> *in Powershell eingeben*

```
$CPU = Get-CimInstance Win32_Processor | Select-Object Name, NumberOfCores, MaxClockSpeed
$RAM = Get-CimInstance Win32_PhysicalMemory | Measure-Object -Property Capacity -Sum 
$Disk = Get-CimInstance Win32_LogicalDisk -Filter "DriveType=3" | ForEach-Object {
    [PSCustomObject]@{
        DeviceID = $_.DeviceID
        Size = "{0:N2} GB" -f ($_.Size / 1GB)
        FreeSpace = "{0:N2} GB" -f ($_.FreeSpace / 1GB)
    }
}

"CPU: $($CPU.Name) - $($CPU.NumberOfCores) Kerne - $($CPU.MaxClockSpeed) MHz"
"RAM: {0:N2} GB" -f ($RAM.Sum / 1GB)
$Disk | Format-Table -AutoSize
```

-> *der Code gibt Informationen über CPU, RAM und Festplattenspeicher aus*