# People Functions

## `isusernametaken()`
- Verifies whether a user account with the specified username is already present
- false result indicates that the username is not taken
- list of usernames: if any of the usernames are taken, the result will be true, false means that all of the usernames are available
- both active and deactivated user accounts are referenced
- username parameter is case-sensitive