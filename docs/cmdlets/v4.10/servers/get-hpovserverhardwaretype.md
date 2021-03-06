﻿---
description: Retrieve Server Hardware Type resource(s).
---

# Get-HPOVServerHardwareType

## Syntax

```text
Get-HPOVServerHardwareType
    [-Name <String>]
    [-Model <String>]
    [-ApplianceConnection <Array>]
    [-exportFile <String>]
    [<CommonParameters>]
```

## Description

Obtain a collection of server hardware types.  This includes information about the type of server, adapter layout and features, and possible server BIOS settings.  This cmdlet is also used with the New-HPOVServerProfile cmdlet to retrieve the list of BIOS settings and adapters to configure.

## Examples

###  Example 1 

```text
$sht = Get-HPOVServerHardwareType

```

Return all the server hardware types on the appliance.

###  Example 2 

```text
$shtBL460Gen81 = Get-HPOVServerHardwareType -name "BL460 Gen8 1"

```

Return the "BL460 Gen8 1" server hardware type on the appliance.

## Parameters

### -Name &lt;String&gt;

The name of the server hardware type resource to be returned.  All server hardware type resources will be returned if omitted.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Model &lt;String&gt;

Filter based on Model name.  Supports wildcard search.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -ApplianceConnection &lt;Array&gt;

Aliases [-Appliance]

Specify one or more `[HPOneView.Appliance.Connection]` object(s) or Name property value(s).

Default Value: ${Global:ConnectSessions}

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | (${Global:ConnectedSessions} &vert; ? Default) |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -ExportFile &lt;String&gt;

Aliases [-x, `-export`]

The path where the resource will be exported to, in JSON text format.

| Aliases | x, export |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**None.  You cannot pipe objects to this cmdlet.**_

## Return Values

_**HPOneView.ServerHardwareType [System.Management.Automation.PSCustomObject]**_

Single Server Hardware type


_**System.Collections.ArrayList**_

Multiple Server Hardware types

## Related Links

* [Set-HPOVServerHardwareType](set-hpovserverhardwaretype.md)
