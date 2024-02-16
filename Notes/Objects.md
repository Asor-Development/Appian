# Objects

## Object Security
https://docs.appian.com/suite/help/23.4/object-security.html
- security is made up of two tightly coupled concepts: groups and role maps
### Groups and role maps
- Appian recommends using only groups to set object security
    - allows you to control object access by changing a user's group membership, rather than directly editing the object's role map
- Role maps are mappings between a series of groups or users and their permissions to an object
    - Each object in Appian has just one role map
    - Each object accepts a different set of permission levels in its role map
    - you can set an object's security, by editing its role map
## UUIDs
- a UUID is automatically generated for every object, this UUID will remain the same from one environment to another
    - you can have two different kinds of object with the same name but the UUID will be different