﻿---
description: Import a power device.
---

# Add-HPOVPowerDevice

## Syntax

```text
Add-HPOVPowerDevice
    [<CommonParameters>]
```

## Description

Import a power device (iPDU) to be managed by an HPE OneView appliance.

## Examples

###  Example 1 

```text
Add-HPOVPowerDevice ipdu24.example.com admin password

```

Add the iPDU to the appliance.

## Parameters

### -Hostname &lt;String&gt;

Hostname of the iPDU, either IP Address or FQDN.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Username &lt;String&gt;

{% hint style="warning" %}
This parameter is being deprecated. Please transition to the `-Credential` parameter.
{% endhint %}


Administrator account of the target iPDU.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Password &lt;String&gt;

{% hint style="warning" %}
This parameter is being deprecated. Please transition to the `-Credential` parameter.
{% endhint %}


Account password of the iPDU specified.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Credential &lt;PSCredential&gt;

Use this parameter if you want to provide a PSCredential object instead.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Force &lt;SwitchParameter&gt;

Force the import of the iPDU when currently managed by another HPE OneView appliance.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -TrustLeafCertificate &lt;SwitchParameter&gt;

If the iPDU SSL certificate is not trusted, use this Cmdlet to add the certificate to the appliance trust store.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Async &lt;SwitchParameter&gt;

Use this parameter to immediately return the async task.  By default, the Cmdlet will wait for the task to complete.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -ApplianceConnection &lt;Object&gt;

Aliases [-Appliance]

Specify one `[HPOneView.Appliance.Connection]` object or Name property value.

Default Value: ${Global:ConnectedSessions} | ? Default

| Aliases | Appliance |
| :--- | :--- |
| Required? | False |
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

Async Task resource to monitor progress.


## Related Links

* [Add-HPOVPowerDeviceConnection](add-hpovpowerdeviceconnection.md)
* [Get-HPOVPowerDevice](get-hpovpowerdevice.md)
* [New-HPOVPowerDevice](new-hpovpowerdevice.md)
* [Remove-HPOVPowerDevice](remove-hpovpowerdevice.md)
