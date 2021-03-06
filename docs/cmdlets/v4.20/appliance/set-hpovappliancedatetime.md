﻿---
description: Update Appliance Date/Time Configuration.
---

# Set-HPOVApplianceDateTime

## Syntax

```text
Set-HPOVApplianceDateTime
    [-SyncWithHost]
    [-Locale] <String>
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

```text
Set-HPOVApplianceDateTime
    [-NTPServers] <Array>
    [-PollingInterval] <Int32>
    [-Locale] <String>
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

## Description

Update the appliance Date and Time configuration, including Locale, NTP Servers, and NTP Polling.

Using the -SyncWithHost parameter will set the NTPServers property to null.

## Examples

###  Example 1 

```text
Set-HPOVApplianceDateTime -NTPServers 10.55.1.1,10.54.1.1 -PollingInterval 60

```

This example passes in updated values to set for the appliance networking configuration.

###  Example 2 

```text
Set-HPOVApplianceDateTime -SyncWithHost

```

This example passes in updated values to set for the appliance networking configuration.

## Parameters

### -SyncWithHost &lt;SwitchParameter&gt;

Specify to configure the embedded hypervisor integration agent to sync time with the hypervisor host.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -NTPServers &lt;Array&gt;

Parameter is deprecated.  Please use the Set-HPOVApplianceDateTime Cmdlet.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -PollingInterval &lt;Int32&gt;

The polling interval in seconds the NTP client will use to verify time drift.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value | 0 |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Locale &lt;String&gt;

Specify the language local for the appliance

    * en_US - US English
    * zh_CN - Simplified Chinese
    * ja_JP - Japanese

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPOneView.Appliance.Connection]` object(s) or Name property value(s).

Default Value: ${Global:ConnectSessions} | ? Default

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

_**None.  You cannot pipe objects to this cmdlet.**_

## Return Values

_**HPOneView.Appliance.TaskResource [System.Management.Automation.PSCustomObject]**_

Asyncronous task resource to monitor

## Related Links

* [Get-HPOVApplianceDateTime](get-hpovappliancedatetime.md)
