---
description: Get configured hypervisor managers.
---

# Get-HPOVHypervisorManager

## Syntax

## Description

You can register a hypervisor manager with HPE OneView by providing hostname and credentials in the Hypervisor Managers user interface. The registered hypervisor manager contains preferences, which are used as default hypervisor or cluster settings during hypervisor cluster profile creation. You can modify the hypervisor manager preferences using the edit operation. You can override these values in a hypervisor cluster profile.

A valid hypervisor manager certificate must be added to HPE OneView trust store to be able to successfully communicate with a hypervisor manager.

The user must have an infrastructure administrator privilege to register or update the hypervisor manager resource in HPE OneView. You can assign scopes to the hypervisor manager resource in HPE OneView.

## Examples

### Example 1

```text
Get-HPOVHypervisorManager -Name vcenter.domain.com
```

Get the specified hypervisor manager by resource name.

### Example 2

```text
Get-HPOVHypervisorManager -Version 5.5.0
```

Get all of the configured hypervisor managers that are vSphere 5.5.0.

## Parameters

### -ApplianceConnection &lt;Array&gt;

Aliases \[-Appliance\]

Specify one or more `[HPOneView.Appliance.Connection]` object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases |  |  |
| :--- | :--- | :--- |
| Required? | False |  |
| Position? | Named |  |
| Default value | \(${Global:ConnectedSessions} | ? Default\) |
| Accept pipeline input? |  |  |
| Accept wildcard characters? |  |  |

### -Label &lt;String&gt;

Specify the label associated with resources.

| Aliases |  |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? |  |
| Accept wildcard characters? |  |

### -Name &lt;String&gt;

Filter for vCenter name.

| Aliases |  |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? |  |
| Accept wildcard characters? |  |

### -Scope &lt;Object&gt;

Filter resources based on provided Scope membership. By default, all resources for the accounts Active Permissions will be displayed. Allowed values:

* AllResources

  \*AllResourcesInScope

* `[HPOneView.Appliance.ScopeCollection]`
* `[HPOneView.Appliance.ConnectionPermission]`

| Aliases |  |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | AllResourcesInScope |
| Accept pipeline input? |  |
| Accept wildcard characters? |  |

### -Version &lt;String&gt;

Filter for specific vCenter version.

| Aliases |  |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? |  |
| Accept wildcard characters? |  |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**None. You cannot pipe objects to this cmdlet.**_

## Return Values

_**HPOneView.Cluster.HypervisorManager**_

The configured hypervisor cluster manager and its properties

## Related Links

* [Add-HPOVHypervisorManager](https://github.com/HewlettPackard/POSH-HPOneView-docs/tree/23d33f2eecfb0193e36ee2bf536a65fa0b258ab2/docs/cmdlets/v4.20/cluster/remove-hpovfabricmanager.md)
* [Remove-HPOVHypervisorManager](remove-hpovhypervisormanager.md)
* [Set-HPOVHypervisorManager](set-hpovhypervisormanager.md)

