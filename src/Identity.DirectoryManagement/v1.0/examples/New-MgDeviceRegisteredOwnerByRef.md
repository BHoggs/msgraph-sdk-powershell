### Example 1: Code snippet

```powershell
Import-Module Microsoft.Graph.Identity.DirectoryManagement

$params = @{
	"@odata.id" = "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}

New-MgDeviceRegisteredOwnerByRef -DeviceId $deviceId -BodyParameter $params
```
This example shows how to use the New-MgDeviceRegisteredOwnerByRef Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

