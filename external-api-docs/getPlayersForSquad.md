
# Find Players In Squad

Returns array of players that are assigned to given squad

**URL** : `https://api.eliteportal.co.uk/external/v1/getPlayersForSquad`

**Method** : `GET`

**Scopes required** : `read:squads`


## Request Query Parameters

- **id** - ID or Custom ID of the squad

## Request Body

N/A

## Example Response
```json
[
    {
        "squadData": {
            "id": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
            "customId": "squad-1",
            "image": "",
            "parent": "squad_root",
            "name": "Squad 1"
        },
        "playerData": {
            "id": "5f1b7911-a5a3-4812-9aa3-9a1415b1db3a",
            "customId": "player-2",
            "firstName": "Default",
            "lastName": "Player 2",
            "image": "",
            "number": 1,
            "positionArea": "DEF",
            "primaryPosition": "RWB",
            "secondaryPositions": [
                "GK",
                "CB"
            ]
        },
        "status": "AVAILABLE"
    },
    {
        "squadData": {
            "id": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
            "customId": "squad-1",
            "image": "",
            "parent": "squad_root",
            "name": "Squad 1"
        },
        "playerData": {
            "id": "5f1b7911-a5a3-4812-9aa3-9a1415b1db3a",
            "customId": "player-2",
            "firstName": "Default",
            "lastName": "Player 2",
            "image": "",
            "number": 1,
            "positionArea": "DEF",
            "primaryPosition": "RWB",
            "secondaryPositions": [
                "GK",
                "CB"
            ]
        },
        "status": "AVAILABLE"
    },
    {
        "squadData": {
            "id": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
            "customId": "squad-1",
            "image": "",
            "parent": "squad_root",
            "name": "Squad 1"
        },
        "playerData": {
            "id": "50b151a6-0055-4168-a498-e5c60ac8b0d3",
            "customId": "player-3",
            "firstName": "Default",
            "lastName": "Player 3",
            "image": "",
            "number": 1,
            "positionArea": "DEF",
            "primaryPosition": "RWB",
            "secondaryPositions": [
                "GK",
                "CB"
            ]
        },
        "status": "AVAILABLE"
    }
]
```

## Notes

N/A
