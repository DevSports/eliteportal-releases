
# Create User Invites

Creates an invitation to signup to the software. The user will be sent an email containing all details to sign up and download.

**URL** : `https://api.eliteportal.co.uk/external/v1/createUserInvites`

**Method** : `POST`

**Scopes required** : `write:users`


## Request Query Parameters

N/A

## Request Body
### Required fields

 -  **email**: string - Valid user email address 
 -  **licence**: string - Licence type, accepted values are "FULL" and "CANDIDATE"
 -  **expiry**: string - ISO date timestamp of user account expiry date, e.g. 2023-06-24
 -  **permissionGroups**: string[] - Array of Permission Group IDs. Empty array allowed

### Optional fields
 -  **firstName**: string - First Name
 -  **lastName**: string - Last Name

## Example Request

```json
{
"users": [{
  "email": "success@devsports.co.uk",
  "firstName": "Test",
  "lastName": "User",
  "licence": "FULL",
  "expiry": "2023-09-27",
  "permissionGroups": []
},
{
  "email": "fail@devsports.co.uk",
  "firstName": "Test",
  "lastName": "User",
  "licence": "FULL",
  "expiry": "2023-09-27",
  "permissionGroups": []
},
{
  "email": "fail2@devsports.co.uk",
  "firstName": "Test",
  "lastName": "User",
  "licence": "FULL",
  "expiry": "2023-09-27",
  "permissionGroups": []
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
