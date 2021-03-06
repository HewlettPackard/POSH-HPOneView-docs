﻿---
description: Restore a Custom Baseline after Restore of a Backup File.
---

# Restore-HPOVCustomBaseline

## Syntax

```text
Restore-HPOVCustomBaseline
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

## Description

This Cmdlet provides the ability to restore custom SPP Baselines that were created with component hotfixes on the appliance after a backup file restore procedure has completed.  It will search for any custom Baseline resources that are in the "Removed" state, and rebuild the baseline with the associated hotfixes.

The source baseline and associated hotfixes must be present within the Baseline repository.  Use the Add-HPOVBaseline to upload the starting Baseline and hotfixes after restoring the Appliance Backup file, then use this Cmdlet to rebuild the Custom Baseline.

## Examples

###  Example 1 

```text
Restore-HPOVCustomBaseline

```

Restore all Custom Baselines that were previously created on all connected appliances.

## Parameters

### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` object(s) or Name property value(s). If Resource object is provided via Pipeline, the ApplianceConnection property of the object will be used.

| Aliases | Appliance |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value | (${Global:ConnectedSessions} &vert; ? Default) |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**None.  You cannot pipe objects to this Cmdlet.**_

## Return Values

_**HPOneView.Appliance.TaskResource [System.Management.Automation.PSCustomObject]**_

The progress of in-progress or completion result

## Related Links

* [New-HPOVCustomBaseline](new-hpovcustombaseline.md)
