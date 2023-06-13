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
- **squadIds**: Array of squad UUIDs to delete.

## Example request
```json
{
    "squadIds": ["16d7cebf-918c-4b0d-abf1-f92083b68031","96f19b4a-7466-46b1-ad1c-c7a119f48f0e"]
}
```

## Example response
```json
[
    {
        "success": true,
        "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
        "message": "Squad delete success"
    },
    {
        "success": false,
        "squadId": "96f19b4a-7466-46b1-ad1c-c7a119f48f0e",
        "message": "Squad not found"
    }
]
```
