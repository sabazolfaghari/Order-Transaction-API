## Sample Order Transaction API

SampleOrderTransaction is a mock API built in WSO2 Synapse that demonstrates routing and response generation for different order types.
The API reads the orderSystem value from the request payload and returns a sample JSON response for:

  PAYMENT → Simulated payment transaction

  TOPUP → Simulated mobile/data top-up

  ECOMMERCE → Simulated e-commerce order

This repository includes:

- The Synapse API XML configuration

- Example Postman requests & responses

- Anonymized/sample data

## How to Run

1. Deploy in WSO2 EI / Micro Integrator

    Copy SampleOrderTransaction.xml into your WSO2 Synapse api deployment folder.

    Restart WSO2.

2. Test with Postman

Example request:

POST http://localhost:8280/sample/order/transaction/

Content-Type: application/json

 ```bash
{
    "orderSystem": "PAYMENT",
    "orderId": "12345"
}
```

Example success response (200 OK):

 ```bash
{
  "code": 200,
  "message": "OK!"
}
```

Example error response (400 Bad Request):

 ```bash
{
  "code": 400,
  "message": "Bad Request!"
}
```
