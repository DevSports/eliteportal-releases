
# Find Players In Squad

Returns array of players that are assigned to given squad

**URL** : `https://api.eliteportal.co.uk/external/v1/getPlayersForSquad`

**Method** : `GET`

**Scopes required** : `read:squads`


## Request Query Parameters

- **id** - ID of squad

## Request Body

N/A

## Example Response
```json
[
    {
        "squadData": {
            "id": "582e1115-007f-4cd7-8162-a0344b332418",
            "image": "",
            "parent": "squad_root",
            "name": "Development Squad"
        },
        "playerData": {
            "id": "3ddc6115-5ef5-4b77-946f-98c2429cea3f",
            "firstName": "Dev",
            "lastName": "Test",
            "image": "",
            "number": 88,
            "positionArea": "GK",
            "primaryPosition": "GK",
            "secondaryPositions": [
                "CB"
            ]
        },
        "status": "AVAILABLE"
    },
    {
        "squadData": {
            "id": "582e1115-007f-4cd7-8162-a0344b332418",
            "image": "",
            "parent": "squad_root",
            "name": "Development Squad"
        },
        "playerData": {
            "id": "1ddcda15-5ef5-4b47-946f-98c4229cea3f",
            "firstName": "Fernando",
            "lastName": "Torres",
            "image": "",
            "number": 9,
            "positionArea": "FWD",
            "primaryPosition": "ST",
            "secondaryPositions": [
                "LW"
            ]
        },
        "status": "AVAILABLE"
    }
]
```

## Notes

N/A
