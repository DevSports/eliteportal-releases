# Delete Players

Queue the deletion of existing players, removing their custom tab data and removing them from squads.

> **Warning**
This is a destructive operation


**URL** : `https://api.eliteportal.co.uk/external/v1/deletePlayers`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body
```json
{
    "playerIds": string[]
}
```

### Required Fields
- **playerIds**: Array of player UUIDs to delete.

## Example request
```json
{
    "playerIds": ["dee95858-86d3-4a84-854e-0b5755560081","76c15145-8b7b-4e2d-9bf9-49bbc142aa21"]
}
```

## Example response
```json
[
    {
        "success": true,
        "playerId": "dee95858-86d3-4a84-854e-0b5755560081",
        "message": "Player delete queued"
    },
    {
        "success": false,
        "playerId": "76c15145-8b7b-4e2d-9bf9-49bbc142aa21",
        "message": "Player not found"
    }
]
