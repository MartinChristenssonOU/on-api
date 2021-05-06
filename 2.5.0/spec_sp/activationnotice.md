# Activation Notice

This API is intended to be used to notify the SP that the CO have activated a service. It is not possible to reject a
subscription through this API. To disconnect a subscription that is unwanted an order, a disconnect order needs to be
sent through the CO order API.

```json
{
  "coId": "Acme",
  "coOrderId": "f3f26446f6e8407aae876ea8e52d7417",
  "coAccessId": "8732c2f065e2490babce820e94b1011a",
  "products": [
    {
      "productId": "8732c2f065e2490babce820e94b1011a",
      "offeringId": "xxx",
      "coProduct": "100/10",
      "coSubscriptionId": "35738e19ab534dff9f9becb3a064a7d5"
    }
  ],
  "orderDateTime": "2021-05-03T20:31:15Z",
  "requestedDateTime": "2021-05-06T00:01:00Z",
  "customerDetails": {
    "identifiedCustomer": true,
    "personalIdentityNumber": "string",
    "customerFirstname": "string",
    "customerLastName": "string",
    "customerPhone": "string",
    "customerMobilePhone": "string",
    "customerEmail": "string",
    "invoiceDetails": {
      "streetName": "string",
      "streetNumber": "string",
      "streetLittera": "string",
      "postalCode": "string",
      "city": "string"
    }
  }
}
```

## products.coProduct

Optional Used to verify that the correct order is active

## coProduct

Represents service in CO api.

HTTP/1.1 200 OK Content-Type: application/json

Standard fel enligt gammal dok