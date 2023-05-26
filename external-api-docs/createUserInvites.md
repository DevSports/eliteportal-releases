
# Create User Invites

Creates an invitation to signup to the software. The user will be sent an email containing all details to sign up and download.

**URL** : `https://api.eliteportal.co.uk/external/v1/createUserInvites`

**Method** : `POST`

**Scopes required** : `write:users`


## Request Query Parameters

N/A

## Request Body

```json
{
   users: [{
	  email: string
	  firstName: string, //Optional
	  lastName: string,
	  licence: "FULL" | "CANDIDATE",
	  expiry: string, //ISO timestamp
	  permissionGroups: string[], //Course codes
	 }]
}
```

## Example Response
```json
[
    {
        "email": "success@devsports.co.uk",
        "success": true,
        "message": "Successfully created user invite"
    },
    {
        "email": "fail@devsports.co.uk",
        "success": false,
        "message": "User already has an account"
    },
    {
        "email": "fail2@devsports.co.uk",
        "success": false,
        "message": "User already has a pending invite"
    }
]
```

## Notes

N/A
