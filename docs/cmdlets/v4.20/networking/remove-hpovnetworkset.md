﻿---
description: Remove a network set.
---

# Remove-HPOVNetworkSet

## Syntax

```text
Remove-HPOVNetworkSet
    [-NetworkSet] <Object>
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

## Description

Delete a network set and its corresponding default connection type.

## Examples

###  Example 1 

```text
$task = Remove-HPOVNetworkSet -networkSet "MyNetSet"
Wait-HPOVTaskComplete $task
```

Remove the network set specifed by name.  Wait for remove to complete.

###  Example 2 

```text
$netSet = Get-HPOVNetworkSet -name "MyNetSet" | Remove-HPOVNetwork

```

Remove the specified network set.

###  Example 3 

```text
Get-HPOVNetworkSet | Remove-HPOVNetworkSet

```

Search for all network sets and remove them from appliance.

## Parameters

### -NetworkSet &lt;Object&gt;

The network set object(s), name(s) or uri(s) to be deleted.  If providing a URI, you must specify an Applinace Connection.

| Aliases | uri, name |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | true (ByValue) |
| Accept wildcard characters? | False |

### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` object(s) or Name property value(s). If Resource object is provided via Pipeline, the ApplianceConnection property of the object will be used.

| Aliases | Appliance |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value | (${Global:ConnectedSessions} &vert; ? Default) |
| Accept pipeline input? | true (ByPropertyName) |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**HPOneView.Networking.NetworkSet [System.Management.Automation.PSCustomObject]**_

Network Set resource object

## Return Values

_**HPOneView.Appliance.TaskResource [System.Management.Automation.PSCustomObject]**_

Removal task

## Related Links

* [Get-HPOVNetworkSet](get-hpovnetworkset.md)
* [New-HPOVNetworkSet](new-hpovnetworkset.md)
* [Set-HPOVNetworkSet](set-hpovnetworkset.md)
