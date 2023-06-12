# Create Players (Under construction)

Create player records in the player pool, can assign them to a squad  

**URL** : `https://api.eliteportal.co.uk/external/v1/createPlayers`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

N/A

## Request Body

```json
{
 "players":
 [
  {
   "firstName": string,
   "lastName": string,
   "number": number,
   "positionArea": string,
   "primaryPosition": string,
   "secondaryPositions": string[],
   "dob": string,
   "squadId": string,
   "footedness": string,
   "nationalTeam": string,
   "height": number,
   "weight": number,
   "image": string
  }
 ]
}
```

### Required Fields

- **lastName** - Player's last name
- **number** - Player number
- **positionArea** - Preferred position area of the player, accepted values are "GK", "DEF", "MID", "FWD".
- **primaryPosition** - Player's primary position, accepted values are "GK", "CB", "RWB", "RB", "LB", "LWB", "CDM", "CM", "CAM", "RM", "LM", "RW", "LW", "CF", "ST"
- **secondaryPositions** - Array of player's secondary positions, accepted values are "GK", "CB", "RWB", "RB", "LB", "LWB", "CDM", "CM", "CAM", "RM", "LM", "RW", "LW", "CF", "ST"
- **nationalTeam** - Player's national team

### Optional Fields
- **firstName** - Player's first name
- **dob** - Player's date of birth, in ISO date string format e.g. 1991-01-25
- **squadId** - Squad UUID if adding player to an existing squad
- **footedness** - Player's footedness, accepted values are "Right", "Left, "Both"
- **height** - Player's height in cm
- **weight** - Player's weight in kg
- **image** - URL pointing to the player's image. Must be externally accessible


## Example request
```json
{
 "players": 
 [
  {
   "lastName": "Anderson",
   "number": 1,
   "positionArea": "DEF",
   "primaryPosition": "RWB",
   "secondaryPositions": 
    [
     "GK",
      "CB"
    ],
   "dob": "2022-05-10",
   "squadId": "",
   "nationalTeam": "England",
   "height": 180,
   "weight": 80
  }   
 ]
}
```

## Example Response
```json
"Create Players Success"
```

## Notes

N/A
