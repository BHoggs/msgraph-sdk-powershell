### Example 1: Get assignments of a user

```powershell
Import-Module Microsoft.Graph.Education

Get-MgEducationUserAssignment -EducationUserId $educationUserId
```
This example shows how to use the Get-MgEducationUserAssignment Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

### Example 2: Get user assignments with expand submissions

```powershell
Import-Module Microsoft.Graph.Education

Get-MgEducationUserAssignment -EducationUserId $educationUserId -ExpandProperty "submissions"
```
This example shows how to use the Get-MgEducationUserAssignment Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

