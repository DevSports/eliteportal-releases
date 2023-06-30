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
- **playerId** UUID or customId of the player to assign
- **squadId** UUID or customId of the squad
- **type** Accepted values: "Add" or "Remove"

## Example request
```json
{
    "players": [
        {
            "playerId": "player-2",
            "squadId": "squad-1",
            "type": "Add"
        },
           {
            "playerId": "5f1b7911-a5a3-4812-9aa3-9a1415b1db3a",
            "squadId": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
            "type": "Add"
        },
        {       
            "playerId": "player-1",
            "squadId": "squad-1",
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
        "playerId": "5f1b7911-a5a3-4812-9aa3-9a1415b1db3a",
        "playerName": "Default Player 2",
        "squadId": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
        "squadName": "Squad 1",
        "message": "Player added to squad"
    },
    {
        "success": true,
        "playerId": "5f1b7911-a5a3-4812-9aa3-9a1415b1db3a",
        "playerName": "Default Player 2",
        "squadId": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
        "squadName": "Squad 1",
        "message": "Player added to squad"
    },
    {
        "success": true,
        "playerId": "3da8e670-f541-4a80-8f05-d84f31da265f",
        "playerName": "Default Player",
        "squadId": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
        "squadName": "Squad 1",
        "message": "Player removed from squad"
    }
]
```
