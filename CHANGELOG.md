# Changelog for API VBS

## Release Date: 2024-04-10

This version introduces a number of improvements and changes aimed at enhancing usability and response structures. Users are encouraged to review the changes detailed below and update their integration accordingly.

### Changes

#### General Improvements
- **Settings Response Update:** The `GET` request for settings no longer nests the settings within a "settings" key. The response is now directly the settings object.
- **Consistency in Slots and Demo Data:** Similar to other changes, slots and demo data handling now directly return objects, eliminating child arrays for consistency and simplicity.

#### Operations
- **GET 1 Operation Improvement:** Retrieving a single operation (`GET /operation/`) is now more straightforward, with the operation object being returned directly instead of within a child array.
- **Operation Prevalidation Change:** The method for operation prevalidation has been changed from `GET` to `POST`. Ensure to update your requests to reflect this change. Parameters are same, they are just transfered to request body.

#### Appointments
- **Simplified Appointment Retrieval:** The API now returns a single appointment object directly for `GET /appointment/` requests, removing the previous requirement for a child array. Also can find 1 appointment by ID or Reference.
- **Appointment Prevalidation Update:** Payload for `POST /appointment/prevalidation/` have changed, [check endpoint documentation.](https://documenter.getpostman.com/view/15107629/2sA2r9VhiD#6a73ffca-4479-460f-9b53-5ea712f3a608)
- **Appointment Creation Update:** Creating an appointment (`POST 1 appointment`) now requires only the IDs of the necessary fields (Same payload as `POST /appointment/prevalidation/`).


#### Fields and Parameters
- **Fields & Parameters Adjustment:** Certain fields or parameters have been modified to improve clarity and functionality. See endpoint documentation.

### Action Required
Users should review their current API integration setup and make necessary adjustments based on the changes described. Testing in a non-production environment is recommended to ensure compatibility.

### Support
For any questions or assistance regarding these changes, please contact our support team at support.vbsapi@dmslog.io.

