## Receive Ping
Receive Ping from Vendor

### Endpoint
**POST** `/receiveping`

*Get ping information from Vendor. Used to decide bid amount.*

### Content Type

Consumes | Produces
-------- | --------
`application/json` | `application/json`

### Parameters

**body** *(required)*

```json
{
    "vendorId": "<Provided by GMG>",
    "zip": 78746,
    "birthday": "MM/DD/YYYY",
    "tobacco": "Y",
    "gender": "M",
    "src": "your_sub_source_identifier",
    "alliance":
    {
        "allianceId": "gmg_12345",
        "allianceUid": "gmg_u_12345",
        "alliancePartnerId": "gmg_partner_12345"
    },
    "tcpa_token": "tcpa_token_value",
    "tcpa_text": "tcpa_text_value",
}
```

### Responses

**Code** `200`

*Received Ping successfully and submitted bid.*

```json
{
  "response": "success",
  "leadAuctionId": 123456,
  "bid": 22,
  "details": "Thank You"
}
```

**Code** `200`

*Generic failure.*

```json
{
  "response": "failure",
  "details": "Please Set vendorId."
}
```

**Code** `200`

*Quota Reached*

```json
{
  "response": "failure",
  "leadAuctionId": 123456,
  "details": "Quota Reached"
}
```

**Code** `500`

*Server Error*

```json
{
  "message": "Server Error"
}
```
