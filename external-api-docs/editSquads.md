# Edit Squads 

Edit squad data, optionally assign to an existing parent squad

**URL** : `https://api.eliteportal.co.uk/external/v1/editSquads`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body

```json
{
 "squads
 [
  {
   "squadId": string,
   "data":
   {
     "customId": string,
     "name": string,
     "parent": string
   }
  }
 ]
}
```
### Squads array
  ### Required Fields
  - **squadId** - UUID or customId of the squad to edit 
  - **data**
     ### Optional Fields
     - **customId** - Update the squad's customId
     - **name** - Update the squad's name
     - **parent** - Parent squad's UUID or customId


## Example request
```json
{
    "squads": [
    {
        "squadId": "squad-1",
        "data": {
            "name": "Squad 1"
        }
    },
        {
        "squadId": "a9eb287f-200d-4c91-8b77-ac945b5878cf",
        "data": {
            "customId": "squad-2",
            "name": "Squad 1",
            "parent": "squad-1"
        }
    }
]
}
```

## Example Response
```json
[
    {
        "squadId": "e9abced8-7d49-40c8-9a7c-2f01583fe425",
        "success": true,
        "customId": "squad-1",
        "name": "Squad 1",
        "message": "Squad edit success"
    },
    {
        "squadId": "a9eb287f-200d-4c91-8b77-ac945b5878cf",
        "success": true,
        "customId": "squad-2",
        "name": "Squad 1",
        "message": "Squad edit success"
    }
]
```

## Notes

N/A
