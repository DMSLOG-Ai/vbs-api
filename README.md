# API VBS Documentation


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

Before diving into the specific endpoints, it's important to note a crucial requirement for all requests made to the API VBS. Each request must include a `placeId` header. This header ensures that your requests are correctly routed and processed based on the terminal in question.


```
headers : {
    ...
    "x-api-key" : YOUR_API_KEY,
    "placeId" : TERMINAL_PLACE_ID
}
```

For a more detailed API documentation, please refer to [API VBS Documentation](https://documenter.getpostman.com/view/15107629/2sA2r9VhiD#intro).

## Error Handling

All errors returned by the api contain a status code 400 and a json object with the key `error`.
Example : 
```
{
    "error": "Invalid placeId"
}
```


## Examples

[Provide a few example requests and responses to demonstrate how to interact with the API. This could include sample curl commands or code snippets.]


## Support

For support, please email support.vbsapi@dmslog.io.

## Contributing

Paypal : paypal@gmslog.io

Crypto : 0x0320323921890730948384723782398923146

## License

[Specify the license under which the API is provided.]
