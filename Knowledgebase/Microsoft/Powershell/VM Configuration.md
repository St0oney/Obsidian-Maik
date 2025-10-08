-> *Für die Konfiguration von VMs bietet es sich an, diese in Variablen zu speichern*
```
$VM1 = Get-VM -VMName "Name"
```

-> *um eine VM in einen anderen Speicherort zu verschieben (die Pfade müssen noch angepasst werden)*

```
Move-VMStorage -VM $VM1 -DestinationStoragePath "D:\Test\VirtualHDDS"
Move-VMStorage -VM $VM1 -VirtualMachinepath "D:\Test\virtualMachines" -SnapshotFilePath "D:\Test\Snapshot"
```

-> *Speicher Anpassungen*
```
Set-VM -VM $VM1 -DynamicMemory
Set-VM -VM $VM1 -MemoryMinimumBytes 4096MB -MemoryMaximumBytes ...
```

