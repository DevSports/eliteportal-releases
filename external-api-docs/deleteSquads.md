# Delete Squads

Queue the deletion of squads and all their permissions.

> **Warning**
This is a destructive operation


**URL** : `https://api.eliteportal.co.uk/external/v1/deleteSquads`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body
```json
{
    "squadIds": string[]
}
```

### Required Fields
- **squadIds**: Array of squad UUIDs or customIds to delete.

## Example request
```json
{
    "squadIds": ["squad-1","335b46b4-fffe-462b-ab89-ac213d15f997"]
}
```

## Example response
```json
[
    {
        "success": true,
        "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
        "customId": "squad-1",
        "name": "Squad 1",
        "message": "Squad delete success"
    },
    {
        "success": true,
        "squadId": "335b46b4-fffe-462b-ab89-ac213d15f997",
        "customId": "squad-b",
        "name": "Squad B",
        "message": "Squad delete success"
    }
]
```
