### Example 1: Code snippet

```powershellImport-Module Microsoft.Graph.Teams

$params = @{
	topic = "Group chat title update"
}

Update-MgChat -ChatId $chatId -BodyParameter $params
```
This example shows how to use the Update-MgChat Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

