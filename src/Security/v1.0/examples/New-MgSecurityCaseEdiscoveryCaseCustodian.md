### Example 1: Code snippet

```powershellImport-Module Microsoft.Graph.Security

$params = @{
	email = "AdeleV@contoso.com"
}

New-MgSecurityCaseEdiscoveryCaseCustodian -EdiscoveryCaseId $ediscoveryCaseId -BodyParameter $params
```
This example shows how to use the New-MgSecurityCaseEdiscoveryCaseCustodian Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

