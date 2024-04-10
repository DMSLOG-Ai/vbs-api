# Changelog for API Version BVS

## Release Date: 2024-04-10

This version introduces a number of improvements and changes aimed at enhancing usability and response structures. Users are encouraged to review the changes detailed below and update their integration accordingly.

### Changes

#### General Improvements
- **Settings Response Update:** The `GET` request for settings no longer nests the settings within a "settings" key. The response is now directly the settings object.
- **Consistency in Slots and Demo Data:** Similar to other changes, slots and demo data handling now directly return objects, eliminating child arrays for consistency and simplicity.
- 
#### Operations
- **GET 1 Operation Improvement:** Retrieving a single operation (`GET /operation/{id}`) is now more straightforward, with the operation object being returned directly instead of within a child array.
- **Operation Prevalidation Change:** The method for operation prevalidation has been changed from `GET` to `POST`. Ensure to update your requests to reflect this change. Parameters are same, they are just transfered to request body.

#### Appointments
- **Simplified Appointment Retrieval:** The API now returns a single appointment object directly for `GET /appointment/{id}` requests, removing the previous requirement for a child array.
- **Appointment Creation Update:** Creating an appointment (`POST 1 appointment`) now requires only the IDs of the necessary fields.


#### Fields and Parameters
- **Fields Adjustment:** Certain fields have been modified to improve clarity and functionality. See endpoint documentation.
- **Parameters Update:** We've made several updates to the parameters to enhance API interaction. See endpoint documentation.

### Action Required
Users should review their current API integration setup and make necessary adjustments based on the changes described. Testing in a non-production environment is recommended to ensure compatibility.

### Support
For any questions or assistance regarding these changes, please contact our support team at support.vbsapi@dmslog.io.

