﻿---
description: Set appliance Login Message.
---

# Set-OVLoginMessage

## Syntax

```text
Set-OVLoginMessage
    [-Message] <String>
    [-Acknowledgment] <Boolean>
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

```text
Set-OVLoginMessage
    [-Acknowledgment] <Boolean>
    [-ApplianceConnection] <Object>
    [<CommonParameters>]
```

## Description

Configure the Login Message for the connected appliance(s).  You can also set the Acknowledgement to be required.

## Examples

###  Example 1 

```text
Set-OVLoginMessage -Message "************************************
>> *****        WARNING        ********
>> ************************************
>> Updated Message: This management appliance is a company owned asset and provided for the exclusive use of authorized personnel. Unauthorized use or
>> abuse of this system may lead to corrective action including termination, civil and/or criminal penalties."
>> -Acknowledgement $true
```

Set the Login Message from all connected appliances.

###  Example 2 

```text
$Message = "************************************
>> *****        WARNING        ********
>> ************************************
>> Updated Message: This management appliance is a company owned asset and provided for the exclusive use of authorized personnel. Unauthorized use or
>> abuse of this system may lead to corrective action including termination, civil and/or criminal penalties."
>>
Set-OVLoginMessage -Message $Message -Acknowledgment $true 
```

Set the Login Message from the specified appliance connection.

## Parameters

### -Message &lt;String&gt;

The login message to set.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value |  |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -Acknowledgment &lt;Boolean&gt;

Set to True if the login message should be acknowledged before authentication completes.  If set to True, the `COnnect-OVMgmt` Cmdlet will prompt the user to acknowledge the message, if `-LoginAcknowledge` is not provided in the Cmdlet parameters.

| Aliases | None |
| :--- | :--- |
| Required? | True |
| Position? | Named |
| Default value | False |
| Accept pipeline input? | false |
| Accept wildcard characters? | False |

### -ApplianceConnection &lt;Object&gt;

Specify one or more `[HPEOneView.Appliance.Connection]` object(s) or Name property value(s).

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

_**None. You cannot pipe objects to this Cmdlet.**_

## Return Values

_**HPEOneView.Appliance.LoginMessage**_

 If successful, returns a resource

## Related Links

* [Get-OVLoginMessage](../appliance/get-ovloginmessage.md)