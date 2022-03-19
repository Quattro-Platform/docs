# Authorization

## The basics
In Quattro App, every action is mapped to a specific permission or to a general permission. For example, the creation of a new Customer requires the `customers.create` permission, while the update of the configuration parameters requires the generic permission `database.manage`.
You can retrieve the list of the user's permissions via the `/api/v*/me` request; it will return the authenticated user, the current tenant information, the websockets configuration and the list of permissions.

> {note} Your application UI must change according to the permissions that the current user has.

## Permissions
A permission is simple string with the generic format `{model}.{action}`. You can find the list of all the permissions with a brief description in the [permissions page](permissions)

## Roles
Roles are basically a group of permissions that can be assigned to a user, the application logic should not change based on roles but only on permissions. 
You can find the list of all the different roles in the [roles page](roles)