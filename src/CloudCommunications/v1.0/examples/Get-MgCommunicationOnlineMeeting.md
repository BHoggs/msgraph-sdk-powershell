### Example 1: Retrieve an online meeting by videoTeleconferenceId

```powershell
Import-Module Microsoft.Graph.CloudCommunications

Get-MgCommunicationOnlineMeeting -Filter "VideoTeleconferenceId eq '123456789'"
```
This example shows how to use the Get-MgCommunicationOnlineMeeting Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

