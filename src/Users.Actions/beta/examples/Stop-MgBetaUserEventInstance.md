### Example 1: Code snippet

```powershell
Import-Module Microsoft.Graph.Beta.Users.Actions

$params = @{
	Comment = "Cancelling for this week due to all hands"
}

# A UPN can also be used as -UserId.
Stop-MgBetaUserEvent -UserId $userId -EventId $eventId -BodyParameter $params
```
This example shows how to use the Stop-MgBetaUserEventInstance Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

