﻿---
description: Remove configured hypervisor managers. 
---

# Remove-HPOVClusterManager

## Syntax

```text
Remove-HPOVClusterManager
    [-InputObject] <HPOneView.ClusterProfile.HypervisorManager>
    [-Force]
    [-ApplianceConnection <Array>]
    [<CommonParameters>]
```

## Description

You can register a hypervisor manager with HPE OneView by providing hostname and credentials in the Hypervisor Managers user interface. The registered hypervisor manager contains preferences, which are used as default hypervisor or cluster settings during hypervisor cluster profile creation. You can modify the hypervisor manager preferences using the edit operation. You can override these values in a hypervisor cluster profile.

A valid hypervisor manager certificate must be added to HPE OneView trust store to be able to successfully communicate with a hypervisor manager.

The user must have an infrastructure administrator privilege to register or update the hypervisor manager resource in HPE OneView.

## Examples

###  Example 1 

```text
Get-HPOVClusterManager -Name vcenter1.domain.com -ErrorAction Stop | Remove-HPOVClusterManager
```

Remove the specified hypervisor manager.

## Parameters

### -ApplianceConnection &lt;Array&gt;

Specify one or more `[HPOneView.Appliance.Connection]` object(s) or Name property value(s).

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | (${Global:ConnectedSessions} &vert; ? Default) |
| Accept pipeline input? | true (ByPropertyName) |
| Accept wildcard characters? | False |

### -Force &lt;SwitchParameter&gt;

Force delete the resource.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -InputObject &lt;HPOneView.ClusterProfile.HypervisorManager&gt;

The `[HPOneView.ClusterProfile.HypervisorManager]` resource to remove from Get-HPOVClusterManager.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | true (ByValue) |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**HPOneView.ClusterProfile.HypervisorManager**_

The hypervisor manager object from Get-HPOVClusterManager.

## Return Values

_**HPOneView.Appliance.TaskResource [System.Management.Automation.PSCustomObject]**_

Asynchronous task resource to monitor.

## Related Links

* [Add-HPOVClusterManager](add-hpovclustermanager.md)
* [Get-HPOVClusterManager](get-hpovclustermanager.md)
* [Set-HPOVClusterManager](set-hpovclustermanager.md)
