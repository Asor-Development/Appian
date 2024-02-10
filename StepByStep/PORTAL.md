# Portal
- use a portal when the users who you expect to use application are not authenticated Appian users
- the portal can be accessed from outside of appian so unauthenticated users can access it
- users can still interact with some Appian processes from a portal
- portal can be used to write data, such as completing a survey, giving feedback, completing an application etc...
- can **Configure portal as a progressive web app**, which provides a more polished experience for users that want to install the portal on their device
- need to create a **Service Account**
    - acts on behalf of your portal users
    - records, processes, and documents stored in Appian won't be available in your portal until you give your service account access to them
    - make sure the service account doesn't have access to record types that aren't used in your portal
    - system administrators can create a service account directly from the portal object
    - needs initator access to process models


---

## Create A Portal
1. Create a new Portal Object
    - Create Interface
        - can be create from the portal or from Appian Designer
        - to create from portal click **Add Page** under Pages, give it a Title and click create interface, which is indicated by a `+` sign
    - Create Service Account
        - be sure to add the service account to the adminstrators group for access


https://academy.appian.com/#/online-course-player/07769a88-b0b5-44ee-a08b-8f2200355f87