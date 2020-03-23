---
description: Generate or show security mode compatability report.
---

# Show-HPOVApplianceSecurityModeCompatibilityReport

## Syntax

```text
Show-HPOVApplianceSecurityModeCompatibilityReport
    [-TargetSecurityMode] <HPOneView.Appliance.SecurityMode>
    [-UpdateReport]
    [-ApplianceConnection <Array>]
    [<CommonParameters>]
```

## Description

When you are considering switching the cryptography mode for your appliance, Hewlett Packard Enterprise recommends that you run the compatibility report to check for compatibility issues for a chosen cryptography mode. Compatibility reports contain information about the behavior of devices and external servers managed or configured by HPE OneView. The report lists the various resources \(storage devices, network devices, servers, enclosures\) managed by HPE OneView that are not compatible with the chosen cryptography mode. You can use the compatibility reports to:

* Determine the impact of the mode switch on various resources, such as, the appliance certificates, external servers and managed devices. 
* Understand the actions recommended to be taken before switching the cryptography mode of the appliance. Examples:
  * Re-importing a higher strength certificate signed by your certificate authority \(CA\).
  * Configuring the managed device or external server to be compliant with the cryptography mode of HPE OneView.
* Determine the devices or class of devices that cannot be managed by HPE OneView in the target mode. Running this Cmdlet will generate a new compatibility report if one does not exist. Use the -UpdateReport switch to generate a new report.

## Examples

### Example 1

```text
$TargetSecurityMode = Get-HPOVApplianceAvailableSecurityMode -ModeName CNSA
Show-HPOVApplianceSecurityModeCompatibilityReport -TargetSecurityMode $TargetSecurityMode
```

Generate a compatibility report for changing the appliance mode to CNSA.

## Parameters

### -ApplianceConnection &lt;Array&gt;

Aliases \[-Appliance\]

Specify one or more `[HPOneView.Appliance.Connection]` object\(s\) or Name property value\(s\).

Default Value: ${Global:ConnectedSessions} \| ? Default

| Aliases | Appliance |  |
| :--- | :--- | :--- |
| Required? | False |  |
| Position? | Named |  |
| Default value | \`\(${Global:ConnectedSessions} | ? Default\)\` |
| Accept pipeline input? | true \(ByPropertyName\) |  |
| Accept wildcard characters? | False |  |

### -TargetSecurityMode &lt;HPOneView.Appliance.SecurityMode&gt;

Specify the target security mode to test resources from `Get-HPOVApplianceAvailableSecurityMode`.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | true \(ByValue\) |
| Accept wildcard characters? | False |

### -UpdateReport &lt;SwitchParameter&gt;

Specify to regenerate the report.

| Aliases | None |
| :--- | :--- |
| Required? | False |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### &lt;CommonParameters&gt;

This cmdlet supports the common parameters: Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer, PipelineVariable, and OutVariable. For more information, see about\_CommonParameters \([http://go.microsoft.com/fwlink/?LinkID=113216](http://go.microsoft.com/fwlink/?LinkID=113216)\)

## Input Types

_**HPOneView.Appliance.SecurityMode**_

Available security mode from [`Get-HPOVApplianceAvailableSecurityMode`](get-hpovapplianceavailablesecuritymode.md).

## Return Values

_**HPOneView.Appliance.SecurityModeCompatibilityReport**_

Security mode compatibility report.

## Related Links
