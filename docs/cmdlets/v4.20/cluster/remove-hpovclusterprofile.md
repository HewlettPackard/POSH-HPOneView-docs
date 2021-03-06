﻿---
description: Remove a cluster profile resource.
---

# Remove-HPOVClusterProfile

## Syntax

```text
Remove-HPOVClusterProfile
    [-InputObject] <Object>
    [-Force]
    [-ApplianceConnection <Object>]
    [<CommonParameters>]
```

## Description

A cluster profile enables you to deploy and manage a cluster of servers (nodes) managed by HPE OneView and orchestrates consistent configuration on cluster of server nodes to share the same workload.  A cluster profile and the associated server profile template are used to define a consistent configuration from server nodes to members in the cluster. The associated server profiles define physical server configurations for server nodes in the cluster, which are derived from parent cluster profile and its associated server profile template.

{% hint style="info" %}
The server profile template must have a configured connection to the hypervisor management network for the template to be valid for use by a hypervisor cluster profile.
{% endhint %}


The cluster profile helps you manage life cycle operations, such as growing or shrinking the cluster, modifying configurations based on needs, consistency checks, and nondisruptive firmware updates on the member nodes. For example, you can grow or shrink a cluster by adding or removing members from the cluster profile. Any change in the configuration of the cluster profile will be reported as an inconsistency. When inconsistencies are remediated, the changed configurations can be applied on cluster and member nodes.

A cluster profile can manage VMware ESXi-based hypervisor clusters by leveraging VMware vCenter server. A hypervisor cluster must be managed by one instance of HPE OneView to avoid inconsistencies.

Use this Cmdlet to remove a cluster profile within OneView.  Removing a cluster within OneView will also destroy the cluster within the cluster manager.

Privileges: Infrastructure administrator, Server administrator, Server profile architect, or Server profile administrator.

## Examples

###  Example 1 

```text
Get-HPOVClusterProfile -Name ProdCluster1 | Remove-HPOVClusterProfile

```

Remove the specified cluster profile.

## Parameters

### -ApplianceConnection &lt;Object&gt;

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

### -InputObject &lt;Object&gt;

The cluster profile from Get-HPOVClusterProfile.

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

_**HPOneView.Cluster.ClusterProfile [System.Management.Automation.PSCustomObject]**_

Cluster profile resource from Get-HPOVClusterProfile.

## Return Values

_**HPOneView.Appliance.TaskResource [System.Management.Automation.PSCustomObject]**_

Asyncronous task resource to monitor.

## Related Links

* [Get-HPOVClusterProfile](get-hpovclusterprofile.md)
* [New-HPOVClusterProfile](new-hpovclusterprofile.md)
* [New-HPOVClusterProfileMember](new-hpovclusterprofilemember.md)
* [Update-HPOVClusterProfile](update-hpovclusterprofile.md)
