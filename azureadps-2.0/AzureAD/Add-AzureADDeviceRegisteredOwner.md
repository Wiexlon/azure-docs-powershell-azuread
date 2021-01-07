---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Add-AzureADDeviceRegisteredOwner

## SYNOPSIS
Adds a registered owner for a device.

## SYNTAX

```
Add-AzureADDeviceRegisteredOwner -ObjectId <String> -RefObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADDeviceRegisteredOwner cmdlet adds a registerd owner for an Azure Active Directory device.

## EXAMPLES

### Example 1: Add a user as a registered owner
```
PS C:\> $User = Get-AzureADUser -Top 1
PS C:\> $Device = Get-AzureADDevice -Top 1
PS C:\> Add-AzureADDeviceRegisteredOwner -ObjectId $Device.ObjectId -RefObjectId $User.ObjectId
```

The first command gets a user by using the Get-AzureADUser (./Get-AzureADUser.md)cmdlet, and then stores it in the $User variable.

The second command gets a device by using the Get-AzureADDevice (./Get-AzureADDevice.md)cmdlet, and then stores it in the $Device variable.

The final command adds the user in $User as the registered owner for the device in $Device. 
Both parameters use the ObjectId property of specified object.


## PARAMETERS

### -ObjectId
Specifies the object ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -RefObjectId
Specifies the ID of the Active Directory object to add.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDeviceRegisteredOwner]()

[Remove-AzureADDeviceRegisteredOwner]()

