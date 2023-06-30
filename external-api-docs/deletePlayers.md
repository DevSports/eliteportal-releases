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
- **playerIds**: Array of player UUIDs or customIds to delete.

## Example request
```json
{
    "playerIds": ["1eb10594-9ce1-43f9-a79a-46054d112d93", "player-2"]
}
```

## Example response
```json
[
    {
        "success": true,
        "playerId": "1eb10594-9ce1-43f9-a79a-46054d112d93",
        "customId": "player-1",
        "name": "Default Player",
        "message": "Player delete queued"
    },
    {
        "success": true,
        "playerId": "4435fdf0-6752-464d-9844-d9e923e96e6c",
        "customId": "player-2",
        "name": "Default Player 2",
        "message": "Player delete queued"
    }
]
```
