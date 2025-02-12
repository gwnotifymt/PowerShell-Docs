---
external help file: Get-DscConfigurationStatus.cdxml-help.xml
Locale: en-US
Module Name: PSDesiredStateConfiguration
ms.date: 06/09/2017
online version: https://docs.microsoft.com/powershell/module/psdesiredstateconfiguration/get-dscconfigurationstatus?view=powershell-5.1&WT.mc_id=ps-gethelp
schema: 2.0.0
title: Get-DscConfigurationStatus
---

# Get-DscConfigurationStatus

## Synopsis
Retrieves data about completed configuration runs.

## Syntax

```
Get-DscConfigurationStatus [-All] [-CimSession <CimSession[]>] [-ThrottleLimit <Int32>] [-AsJob]
 [<CommonParameters>]
```

## Description
The **Get-DscConfigurationStatus** cmdlet retrieves detailed information about completed configuration runs on the system.
By default, it returns the information about the last configuration run.
This cmdlet is useful for finding historical information about configuration runs, such as when the configurations were run, the status of the runs, the number of resources in the configurations, and which resources succeeded or failed.

## Examples

### Example 1: Get information on the last configuration run

```
PS C:\> Get-DscConfigurationStatus
```

This command gets information on the last configuration run.

### Example 2: Get information on all configurations

```
PS C:\> Get-DscConfigurationStatus -All
```

This command gets information about all the configurations that were run on the system, including the Windows PowerShell Desired State Configuration (DSC) consistency check.

### Example 3: Get information on the configuration run on a remote computer

```
PS C:\> Get-DscConfigurationStatus -CimSession "Server01"
```

This command gets the configuration run details of the remote computer named Server01.
This uses the WSMan transport to connect to the remote computer and requires that the connecting user be an administrator on the remote computer.

## Parameters

### -All
Indicates that this cmdlet retrieves information about all the configuration runs on the computer, including the configuration application and the consistency check.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Indicates that this cmdlet runs the command as a background job.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a [New-CimSession](/powershell/module/cimcmdlets/new-cimsession) or [Get-CimSession](/powershell/module/cimcmdlets/get-cimsession) cmdlet.
The default is the current session on the local computer.

```yaml
Type: Microsoft.Management.Infrastructure.CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

## Outputs

## Notes

## Related links

[Windows PowerShell Desired State Configuration Overview](/powershell/scripting/dsc/overview/dscforengineers)

[Get-DscConfiguration](Get-DscConfiguration.md)

[Get-DscLocalConfigurationManager](Get-DscLocalConfigurationManager.md)

[Restore-DscConfiguration](Restore-DscConfiguration.md)

[Start-DscConfiguration](Start-DscConfiguration.md)

[Test-DscConfiguration](Test-DscConfiguration.md)
