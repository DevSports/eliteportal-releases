
# Query Sessions

Get details about created sessions

**URL** : `https://api.eliteportal.co.uk/external/v1/getSessions`

**Method** : `GET`

**Scopes required** : `read:sessions`


## Request Query Parameters

 -  **squadId**: string - ID of squad - Optional
  - **updatedStartDate**: string - Last updated greater than in ISO timestamp format - Optional
  - **updatedEndDate**: string - Last updated less than in ISO timestamp format - Optional
  - **scheduledStartDate**: string - Scheduled date greater than in ISO timestamp format - Optional
  - **scheduledEndDate**: string - Scheduled date less than in ISO timestamp format - Optional

## Request Body

N/A

## Example Response
```json
[
    {
        "owner": "SdTWTCQB2zvuBZmJk84lgPthkRK8",
        "notes": "Session\n\n\notes \n\n\test",
        "updatedAt": "2023-05-26T09:58:32.181Z",
        "createdAt": "2023-05-26T09:54:52.396Z",
        "schedule": {
            "startDate": "",
            "endDate": "",
            "isScheduled": false,
            "markedComplete": false
        },
        "total": {
            "restTime": 60,
            "totalTime": 180,
            "activeTime": 120
        },
        "deleted": false,
        "squad": {
            "squadId": "9521a93a-1e35-4983-9f43-e8bf4ca9ef8f",
            "image": "",
            "name": "Development Squad",
            "players": [
                {
                    "firstName": "Dev",
                    "lastName": "Test",
                    "number": 88,
                    "image": "",
                    "positionArea": "GK",
                    "playerId": "895ef629-c035-4314-9545-9885ba08af06",
                    "primaryPosition": "GK",
                    "height": 0,
                    "status": "AVAILABLE"
                }
            ]
        },
        "exerciseFields": [
            {
                "show": true,
                "value": "Custom text value here",
                "fieldId": "56aa7753-696d-4523-97c3-8e3b61dd7af6"
            },
            {
                "show": true,
                "value": "2",
                "fieldId": "91972f50-1bb4-4c3c-acd3-2c56a961b97c"
            }
        ],
        "slides": [
            {
                "id": "27388358-528a-4921-8ef4-5571acbfb66a",
                "rest": 60,
                "reps": "1",
                "time": 120,
                "notes": "Notes notes notes",
                "players": [
                    "895ef629-c035-4314-9545-9885ba08af06"
                ],
                "name": "Session Animation",
                "items": [
                    {
                        "id": "5b7aece8-3a9a-43ec-adcc-d0462c28dd0d",
                        "documentid": "742af68a-b77f-42a0-b808-af8cc0d4db73",
                        "type": "ANIMATION"
                    }
                ],
                "exerciseFields": [
                    {
                        "show": true,
                        "value": "Animation custom field text",
                        "fieldId": "56aa7753-696d-4523-97c3-8e3b61dd7af6"
                    },
                    {
                        "show": true,
                        "value": "1",
                        "fieldId": "91972f50-1bb4-4c3c-acd3-2c56a961b97c"
                    }
                ]
            }
        ]
    }
]
```

## Notes

N/A
