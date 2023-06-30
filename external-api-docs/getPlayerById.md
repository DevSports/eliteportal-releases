# Get Player By ID

Get details of player of given ID

**URL** : `https://api.eliteportal.co.uk/external/v1/getPlayerById`

**Method** : `GET`

**Scopes required** : `read:squads`


## Request Query Parameters

 - **id** - ID or Custom ID of the player

## Request Body

N/A

## Example Response
```json
{
    "id": "8f3cab2e-9fb0-4d95-ba9a-294165326e16",
    "customId": "custom-id",
    "name": "Dev Test",
    "firstName": "Dev",
    "lastName": "Test",
    "number": 88,
    "positionArea": "GK",
    "primaryPosition": "GK",
    "secondaryPositions": [
        "CB"
    ],
    "dob": "2000-08-09T23:42:57+0000",
    "nationalTeam": "England",
    "height": 0,
    "weight": 0,
    "footedness": "Both",
    "image": "",
    "createdAt": "2023-06-29T11:16:14.383Z",
    "updatedAt": "2023-06-29T11:16:14.383Z"
}
```

## Notes

N/A
