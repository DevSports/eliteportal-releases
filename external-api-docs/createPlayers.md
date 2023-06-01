# Create Players (Under construction)

Create player records in the player pool. Assigning them one or multiple squads  
// todo multiple

**URL** : `https://api.eliteportal.co.uk/external/v1/createPlayers`

**Method** : `POST`

**Scopes required** : `write:squads`

## Request Query Parameters

## Request Body
```json
{
"players": [
  "playerType": string; // "INTERNAL" | "EXTERNAL"
  firstName: string;
  lastName: string;
  number: number;
  positionArea: TPositionArea;
  primaryPosition: TPlayerPosition;
  secondaryPositions: IPlayerPositionFamiliarity[];
  rating: number;
  dob: string;
  squadId: string;
  footedness: TFootedness;
  nationalTeam: string;
  height: number;
  weight: number;
  image: string;
]
}
```

N/A

## Example Response
```json
```

## Notes

N/A
