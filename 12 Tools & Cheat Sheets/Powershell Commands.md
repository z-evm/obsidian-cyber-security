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

######  **Identify Wi-Fi module**
```
Get-PnpDevice -Class Net | Where-Object { $_.FriendlyName -like "*Wi-Fi*" -or $_.FriendlyName -like "*Wireless*" } | Select-Object -Property FriendlyName, InstanceId
```

##### **Identify Bluetooth Adapter**
```
Get-PnpDevice -Class Bluetooth | Where-Object { $_.FriendlyName -like "*Bluetooth*" } | Select-Object -Property FriendlyName, InstanceId
```

**Identify GPU/s**
```
wmic path win32_VideoController get name, driverVersion
```