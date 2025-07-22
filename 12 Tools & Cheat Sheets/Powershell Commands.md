###### **View RAM Specifications**

```
Get-CimInstance -ClassName Win32_PhysicalMemory | Select-Object BankLabel, Capacity, Manufacturer, Speed, SerialNumber, PartNumber
```

###### **View SSD Specifications**

```
Get-Disk | Select-Object Number, FriendlyName, SerialNumber, BusType, Size
```

###### **Check Battery Model**

```
Get-WmiObject -Class Win32_Battery | Select-Object Name, BatteryStatus, EstimatedChargeRemaining
```

