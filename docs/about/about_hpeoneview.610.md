﻿TOPIC

    about_HPEOneView.610

COPYRIGHT

    (C) Copyright 2013-2021 Hewlett Packard Enterprise Development LP

LICENSE

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.

SHORT DESCRIPTION

    PowerShell library for HPE OneView 6.10

WHAT'S NEW

   Release 6.10.2775.2226

      -- Initial HPE OneView 6.10 library release.
      -- Deprecated Invoke-OVVcmMigration as the functionality was removed from HPE OneView 5.40.
      -- [#564] Fixed Set-OVSmtpConfig to send a properly formatted request to the appliance
         REST API to disable email alert filters.
      -- Added -UseMXRecordLookup to Set-OVSmtpConfig Cmdlet to allow for DNS MX record lookup
         to be used instead of specifying an SMTP server with the -Server parameter.
      -- Enhanced Get-OVServer to return expanded server hardware inventory. This now fully populates
         the subResources property with available inventory data.
      -- [#512] Fixed Set-OVUplinkSet to add and remove associated networks when adding/removing network
         set(s).
      -- Added Windows Server 2019 and Ubuntu values for HostOStype parameter within New-OVServerProfile,
         New-OVServerProfileTemplate and New-OVServerProfileAttachVolume Cmdlets.
      -- [#569] Refactored detection of duplicate JSON pattern in API response, mainly with FW baselines/SPPs.

LONG DESCRIPTION

    This library provides HP OneView management capabilities for Windows PowerShell.
    The library can be used as either a CLI or using the core cmdlets to call from
    wrapper scripts.  The core cmdlets are:

      -- Connect-OVMgmt
      -- Send-OVRequest
      -- New-OVResource
      -- Set-OVResource
      -- Remove-OVResource

    A set of sample scripts are also provided, that show how to fully configure an
    HP OneView appliance from the ground up.

    For information regarding this project, to request features or report
    issues, please see: https://github.com/HewlettPackard/POSH-HPEOneView/issues


SEE ALSO

    https://github.com/HewlettPackard/POSH-HPEOneView
    https://hpe-docs.gitbook.io/posh-hpeoneview
    http://hpe.com/info/oneviewcommunity
    Update-Help HPEOneView.610
    Get-Help about_Appliance_Connections
    Get-Help about_Appliance_Connection_Permissions
    Get-Help about_Two_Factor_Authentication
    Get-Help Connect-OVmgmt
    Get-Help Send-OVRequest
    [install_dir]\Samples
