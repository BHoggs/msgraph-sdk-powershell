### Example 1: Get reply to a message in a channel

```powershell
Import-Module Microsoft.Graph.Beta.Teams

Get-MgBetaTeamChannelMessageReply -TeamId $teamId -ChannelId $channelId -ChatMessageId $chatMessageId -ChatMessageId1 $chatMessageId1
```
This example shows how to use the Get-MgBetaTeamChannelMessageReply Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).

