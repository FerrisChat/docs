# MemberRoleDelete

| Field | Type | Description |
| --- | --- | --- |
| member | Member | The member this role was removed from |
| role | Role | The role that was removed from this member |

```json
{
  "c":"RoleUpdate",
  "d":{
    "member":{type Member},
    "role":{type Role}
  }
}
```