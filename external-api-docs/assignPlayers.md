# Assign Players

Assign or remove players from squads

**URL** : `https://api.eliteportal.co.uk/external/v1/assignPlayers`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body
```json
{
"players": 
 [
  playerId: string,
  squadId: string,
  type: string 
 ]
}
```

### Required Fields
- **playerId** UUID of the player to assign
- **squadId** UUID of the squad
- **type** Accepted values: "Add" or "Remove"

## Example request
```json
{
    "players": [
        {
            "playerId": "a7c03e0e-9d95-4b9b-900f-9ec99b9b9268",
            "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
            "type": "Add"
        },
        {
            "playerId": "a7c03e0e-9d95-4b9b-900f-9ec99b9b9268",
            "squadId": "ea9c1c35-8558-49c7-985e-290ebc409bfd",
            "type": "Add"
        },
                {
            "playerId": "a5cdd23d-25bb-4287-9070-c1437a007caa",
            "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
            "type": "Remove"
        }
    ]
}
```

## Example Response
```json
[
    {
        "success": true,
        "playerId": "a7c03e0e-9d95-4b9b-900f-9ec99b9b9268",
        "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
        "message": "Player added to squad"
    },
    {
        "success": false,
        "playerId": "a7c03e0e-9d95-4b9b-900f-9ec99b9b9268",
        "squadId": "ea9c1c35-8558-49c7-985e-290ebc409bfd",
        "message": "Squad doesn't exist"
    },
    {
        "success": false,
        "playerId": "a5cdd23d-25bb-4287-9070-c1437a007caa",
        "squadId": "16d7cebf-918c-4b0d-abf1-f92083b68031",
        "message": "Player doesn't exist"
    }
]
```
