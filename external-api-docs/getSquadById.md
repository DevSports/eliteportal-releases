# Get Squad By ID

Get details of squad of given ID

**URL** : `https://api.eliteportal.co.uk/external/v1/getSquadById`

**Method** : `GET`

**Scopes required** : `read:squads`


## Request Query Parameters

 - **id** - ID or Custom ID of the squad

## Request Body

N/A

## Example Response
```json
{
  "id": "cad2976a-4bf1-420f-bfb9-7dbe0ba2c20d",
  "customId": "my-custom-id"
  "name": "Development Squad",
  "squadType": "INTERNAL",
  "image": "",
  "deleted": false,
  "parent": "squad_root",
  "notes": "",
  "createdAt": "2023-05-25T14:36:21.290Z",
  "updatedAt": "2023-05-25T14:36:21.290Z"
}
```

## Notes

N/A
