### Example 1: Get a user's one on one chat

```powershell
Import-Module Microsoft.Graph.Teams

Get-MgUserChat -UserId $userId -ChatId $chatId
```
This example shows how to use the Get-MgUserChat Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

