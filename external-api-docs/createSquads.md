# Create Squads 

Create squads and assign them users or assign them to permission groups

**URL** : `https://api.eliteportal.co.uk/external/v1/createSquads`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body

```json
{
  "squads":
  [
    {
      "name": string,
      "customId": string,
      "image": string,
      "parentId": string,
      "permissionGroups":
      [
       {
        "permissionGroupId": string,
        "access": string
       }
      ],
      "users":
      [
       {
        "userId": string,
        "access": string
       }
      ]
      
    }
  ]
```
### Required Fields

- **name** - Squad name

### Optional Fields
- **customId** - Custom ID used for queries
- **image** - URL pointing to the squad's image. Must be externally accessible
- **parentId** - ID of parent squad to assign to, inheriting its permissions
- **permissionGroups** - Array of objects containing permission group IDs and access level. Accepted access level values are "READ", "WRITE", "ADMIN"
- **users** - Array of objects containing user IDs and access level. Accepted access level values are "READ", "WRITE", "ADMIN"

## Example request
```json
{
    "squads": [
        {
            "name": "Squad 1",
            "image": "",
            "customId": "squad-1",
            "users": [{
                "userId": "iXZmL8KKCnpkdPbjOMPGUOHP781W",
                "access": "WRITE"
            }],
            "permissionGroups": [{
                "permissionGroupId": "43371bb6-f3a8-41c3-aa26-b28fcf3ba605",
                "access": "READ"
            }]
        }
    ]
}
```
## Example response
```json
[
    {
        "success": true,
        "squadId": "1bad0e4c-694e-427f-99e8-376b13723814",
        "message": "Squad create success"
    }
]
```
