# Set-BcdBootDefault

## SYNOPSIS
Sets the default boot entry for the boot configuration data store.

## SYNTAX

### Id
```
Set-BcdBootDefault [-Id] <String> [[-Store] <BcdStoreInfo>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Entry
```
Set-BcdBootDefault [-Entry] <BcdEntryInfo> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The Set-BcdBootDefault cmdlet sets the default boot entry for the boot configuration data store. This cmdlet updates the BootMgr object in the boot configuration data store.

## EXAMPLES

### EXAMPLE 1

```powershell
Set-BcdBootDefault -Id {bootmgr}
```

Sets the default boot entry to the Windows boot manager.

### EXAMPLE 2

```powershell
Set-BcdElement -Store C:\BCD -Id {GUID}
```

### EXAMPLE 3

```powershell
Set-BcdElement -Store C:\BCD -Entry {bootmgr}
```

## PARAMETERS

### Id
Specifies the identifier of the boot entry or boot application element that you want to modify. The identifier can be a globally unique identifier (GUID) or a friendly identifier.

```yaml
Type: String
Parameter Sets: Id
Aliases: Identifier

Required: true
Position: 0
Default Value: 
Pipeline Input: True (ByPropertyName, ByValue)
```

### Store
Specifies the path to the boot configuration data store (BCD) that you want to modify. The BCD store is a database that contains boot configuration data and controls the boot process on a computer.

```yaml
Type: BcdStoreInfo
Parameter Sets: Id
Aliases: 

Required: false
Position: 1
Default Value: 
Pipeline Input: False
```

### Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: false
Position: named
Default Value: 
Pipeline Input: False
```

### WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: false
Position: named
Default Value: 
Pipeline Input: False
```

### Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: false
Position: named
Default Value: 
Pipeline Input: False
```

### Entry
Specifies the boot entry or boot application element that you want to modify.

```yaml
Type: BcdEntryInfo
Parameter Sets: Entry
Aliases: 

Required: true
Position: 0
Default Value: 
Pipeline Input: True (ByValue)
```

### \<CommonParameters\>
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
Microsoft.Windows.Bcd.Cmdlets.BcdExtensions.BcdEntryInfo


## OUTPUTS

### System.Object


## NOTES

The BootMgr object in the boot configuration data store determines which boot entry is displayed as the default boot entry in the boot menu. The default boot entry is highlighted in the boot  menu and is automatically selected after the default timeout period.

## RELATED LINKS

[Get-BcdEntry]()

[Get-BcdStore]()

[Set-BcdBootSequence]()

[Set-BcdBootTimeout]()
