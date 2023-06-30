# Edit Players 

Edit individual fields for existing player records

**URL** : `https://api.eliteportal.co.uk/external/v1/editPlayers`

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
   "playerId": string,
   "data":
   {
     "customId": string,
     "firstName": string,
     "lastName": string,
     "number": number,
     "positionArea": string,
     "primaryPosition": string,
     "secondaryPositions": string[],
     "dob": string,
     "footedness": string,
     "nationalTeam": string,
     "height": number,
     "weight": number,
     "image": string
   }
  }
 ]
}
```
### Players array
  ### Required Fields
  - **playerId** - UUID or customId of the player to edit 
  - **data**
     ### Optional Fields
     - **customId** - Update this player's customId
     - **firstName** - Player's first name
     - **lastName** - Player's last name
     - **dob** - Player's date of birth, in ISO date string format e.g. 1991-01-25
     - **footedness** - Player's footedness, accepted values are "Right", "Left, "Both"
     - **height** - Player's height in cm
     - **weight** - Player's weight in kg
     - **image** - URL pointing to the player's image. Must be externally accessible
     - **number** - Player number
     - **positionArea** - Preferred position area of the player, accepted values are "GK", "DEF", "MID", "FWD".
     - **primaryPosition** - Player's primary position, accepted values are "GK", "CB", "RWB", "RB", "LB", "LWB", "CDM", "CM", "CAM", "RM", "LM", "RW", "LW", "CF", "ST"
     - **secondaryPositions** - Array of player's secondary positions, accepted values are "GK", "CB", "RWB", "RB", "LB", "LWB", "CDM", "CM", "CAM", "RM", "LM", "RW", "LW", "CF", "ST"
     - **nationalTeam** - Player's national team, please pick one from the country list


## Accepted countries
      `Brazil`,
      `Belgium`,
      `Argentina`,
      `France`,
      `England`,
      `Spain`,
      `Italy`,
      `Netherlands`,
      `Portugal`,
      `Denmark`,
      `Germany`,
      `Mexico`,
      `Uruguay`,
      `United States`,
      `Croatia`,
      `Switzerland`,
      `Colombia`,
      `Senegal`,
      `Wales`,
      `Sweden`,
      `Peru`,
      `Morocco`,
      `Iran`,
      `Japan`,
      `Serbia`,
      `Poland`,
      `Ukraine`,
      `Korea Republic`,
      `Chile`,
      `Tunisia`,
      `Nigeria`,
      `Czech Republic`,
      `Austria`,
      `Costa Rica`,
      `Russia`,
      `Norway`,
      `Hungary`,
      `Cameroon`,
      `Australia`,
      `Egypt`,
      `Algeria`,
      `Turkey`,
      `Canada`,
      `Ecuador`,
      `Scotland`,
      `Mali`,
      `Republic of Ireland`,
      `Greece`,
      `Qatar`,
      `Paraguay`,
      `Slovakia`,
      `Côte d'Ivoire`,
      `Saudi Arabia`,
      `Romania`,
      `Burkina Faso`,
      `Venezuela`,
      `Bosnia-Herzegovina`,
      `Northern Ireland`,
      `Finland`,
      `Ghana`,
      `Panama`,
      `Jamaica`,
      `Iceland`,
      `North Macedonia`,
      `Slovenia`,
      `Albania`,
      `Montenegro`,
      `South Africa`,
      `UAE`,
      `Iraq`,
      `El Salvador`,
      `Cabo Verde`,
      `Congo DR`,
      `Bulgaria`,
      `Oman`,
      `Israel`,
      `Uzbekistan`,
      `China PR`,
      `Gabon`,
      `Honduras`,
      `Bolivia`,
      `Georgia`,
      `Guinea`,
      `Curaçao`,
      `Bahrain`,
      `Jordan`,
      `Haiti`,
      `Zambia`,
      `Syria`,
      `Uganda`,
      `Benin`,
      `Armenia`,
      `Luxembourg`,
      `Palestine`,
      `Kyrgyz Republic`,
      `Belarus`,
      `Vietnam`,
      `Equatorial Guinea`,
      `Congo`,
      `Lebanon`,
      `Trinidad and Tobago`,
      `Kenya`,
      `New Zealand`,
      `India`,
      `Madagascar`,
      `Kosovo`,
      `Cyprus`,
      `Tajikistan`,
      `Estonia`,
      `Mauritania`,
      `Thailand`,
      `Korea DPR`,
      `Sierra Leone`,
      `Kazakhstan`,
      `Guinea-Bissau`,
      `Guatemala`,
      `Namibia`,
      `Mozambique`,
      `Niger`,
      `Libya`,
      `Malawi`,
      `Angola`,
      `Zimbabwe`,
      `Gambia`,
      `Faroe Islands`,
      `Comoros`,
      `Togo`,
      `Azerbaijan`,
      `Latvia`,
      `Sudan`,
      `Tanzania`,
      `Antigua and Barbuda`,
      `Central African Republic`,
      `Philippines`,
      `Turkmenistan`,
      `Rwanda`,
      `Solomon Islands`,
      `Ethiopia`,
      `Nicaragua`,
      `Burundi`,
      `St. Kitts and Nevis`,
      `Lithuania`,
      `Suriname`,
      `Eswatini`,
      `Hong Kong`,
      `Lesotho`,
      `Malaysia`,
      `Kuwait`,
      `Botswana`,
      `Liberia`,
      `Dominican Republic`,
      `Andorra`,
      `Yemen`,
      `Afghanistan`,
      `Indonesia`,
      `Maldives`,
      `Chinese Taipei`,
      `Myanmar`,
      `Singapore`,
      `New Caledonia`,
      `Papua New Guinea`,
      `Tahiti`,
      `Fiji`,
      `Vanuatu`,
      `South Sudan`,
      `Barbados`,
      `Cuba`,
      `Malta`,
      `Puerto Rico`,
      `Bermuda`,
      `Grenada`,
      `Guyana`,
      `St. Lucia`,
      `Cambodia`,
      `Belize`,
      `Nepal`,
      `Montserrat`,
      `Moldova`,
      `Mauritius`,
      `St. Vincent / Grenadines`,
      `Chad`,
      `Macau`,
      `Laos`,
      `Mongolia`,
      `Dominica`,
      `Bhutan`,
      `São Tomé e Príncipe`,
      `American Samoa`,
      `Cook Islands`,
      `Brunei`,
      `Samoa`,
      `Bangladesh`,
      `Djibouti`,
      `Liechtenstein`,
      `Seychelles`,
      `Pakistan`,
      `Cayman Islands`,
      `Tonga`,
      `Timor-Leste`,
      `Somalia`,
      `Gibraltar`,
      `Eritrea`,
      `Aruba`,
      `Bahamas`,
      `Guam`,
      `Turks and Caicos Islands`,
      `Sri Lanka`,
      `US Virgin Islands`,
      `British Virgin Islands`,
      `Anguilla`,
      `San Marino`,



## Example request
```json
{
    "players":
   [
    {
        "playerId": "player-1",
        "data": {
            "customId": "player-1",
            "firstName": "Test",
            "lastName": "Player",
            "number": 1,
            "positionArea": "DEF",
            "primaryPosition": "RB",
            "secondaryPositions": [
                "GK",
                "CB",
                "LWB"
            ],
            "height": 185,
            "weight": 90
        }
    }
   ]
}
```

## Example Response
```json
[
    {
        "playerId": "137b9525-fac0-484e-90fe-2074649888f0",
        "success": true,
        "customId": "player-1",
        "name": "Test Player",
        "message": "Player edit success"
    }
]
```

## Notes

N/A
