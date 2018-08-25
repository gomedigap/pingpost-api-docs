## Receive Post
Receive Post from Vendor

### Endpoint
**POST** `/receivepost`

*Get post information from Vendor. Used to create lead in Mediapp.*

### Content Type

Consumes | Produces
-------- | --------
`application/json` | `application/json`

### Parameters

**body** *(required)*

```json
{
    "leadAuctionId": "654321",
    "ip": "127.0.0.1",
    "firstName": "Johnny",
    "lastName": "Appleseed",
    "email": "johnny.appleseed@example.com",
    "phone": "5551231234",
    "xid": "your_internal_lead_id"
}
```

*Note: leadAuctionId was part of successful Ping response.*

### Responses

**Code** `200`

*Received Post successfully and created lead.*

```json
{
  "response": "success",
  "details": "Thank You"
}
```

**Code** `500`

*Server Error*

```json
{
  "message": "Server Error"
}
```