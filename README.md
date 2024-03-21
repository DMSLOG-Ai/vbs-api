# API VBS Documentation

## Documentation

For a more detailed API documentation, please refer to [API VBS Documentation](https://documenter.getpostman.com/view/15107629/2sA2r9VhiD#intro).

## Introduction

API VBS provides a robust interface for transportation management systems (TMS) to interact seamlessly with vehicle booking systems. It facilitates operations like retrieving settings, prevalidating and executing operations and appointments, and getting available slots. This API is designed to streamline the workflow for carriers by offering detailed information on dispatchers, drivers, trucks, trailers, and appointment scheduling.

## Getting Started

Before you begin, ensure that you have a basic understanding of RESTful principles and HTTP requests. To interact with API VBS, you'll need to have a TMS or a similar system capable of sending HTTP requests.

### Base URL

The API is accessed from the base URL sent in mail.

### Authentication

API VBS utilizes API keys to allow access to the API. We will send you your API key, this is unique to your account and serves as a method to authenticate your requests.
You must include your API key in each request to our API endpoints.

To authenticate with the API VBS, you need to include your API key in the header of each HTTP request. The API key should be included as the value of the `x-api-key` header field.


## API Endpoints

Before diving into the specific endpoints, it's important to note a crucial requirement for all requests made to the API VBS. Each request must include a `placeId` header that specifies the terminal concerned by the request. This header ensures that your requests are correctly routed and processed based on the terminal in question.


headers : {
    ...
    "x-api-key" : YOUR_API_KEY,
    "placeId" : TERMINAL_PLACE_ID
}

### 1. Get Settings

- **Endpoint:** `GET /settings/`
- **Description:** Retrieve your carrier settings.
- **Parameters:** None
- **Response:** A JSON object containing over 100 fields related to manager, dispatchers, drivers, trucks, trailers.

### 2. Operation Prevalidation and Execution

- **Prevalidation Endpoint:** `POST /operation/prevalidation/`
    - **Fields:** 3 fields
    - **Response:** 30 fields including operation details.

- **Execution Endpoint:** `POST /operation/`
    - **Fields:** 30 fields
    - **Response:** 31 fields, operation details plus ID.

### 3. Get Slots

- **Endpoint:** `GET /slots/`
- **Fields:** 1 field
- **Response:** JSON object with 8 slots indicating all-day availability.

### 4. Appointment Prevalidation and Booking

- **Prevalidation Endpoint:** `POST /appointment/prevalidation/`
    - **Fields:** 6 fields
    - **Response:** 50 fields including appointment details.

- **Booking Endpoint:** `POST /appointment/`
    - **Fields:** 50 fields
    - **Response:** 31 fields, appointment details plus ID.

## Error Handling

[Explain how errors are handled and returned by the API.]

## Rate Limiting

[If applicable, describe any rate limits that apply to API requests.]

## Examples

[Provide a few example requests and responses to demonstrate how to interact with the API. This could include sample curl commands or code snippets.]


## Support

For support, please email support.vbsapi@dmslog.io or create an issue in this GitHub repository.

## Contributing

We welcome contributions! Please read our contributing guide to learn how to propose bugfixes, improvements, and new features.

## License

[Specify the license under which the API is provided.]
