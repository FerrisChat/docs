# MemberRoleAdd

| Field | Type | Description |
| --- | --- | --- |
| member | Member | The member this role was added to |
| role | Role | The role that was added to this member |

```json
{
  "c":"RoleUpdate",
  "d":{
    "member":{type Member},
    "role":{type Role}
  }
}
```