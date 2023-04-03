## Events Schema

```json
{
  "$id": "event.schema.json",
  "$schema": "http://json-schema.org/draft-07/schema#",
  "description": "Waste Event Standard Format for describing one event of one waste type",
  "meta:license": [
    "Copyright 2021 Topolytics Ltd. All rights reserved.",
    "EXAMPLE LICENCE"
  ],
  "title": "Topolytics Waste Events Standard - Single Event",
  "type": "object",
  "properties": {
    "device_id": {
      "title": "Device ID",
      "description": "The unique identifier of the device used for scanning items.",
      "type": "string",
      "example": "DID:12345",
      "maxLength": 50
    },
    "device_lng": {
      "title": "Device Longitude",
      "description": "Longitude of where the device is located.",
      "type": "number",
      "example": 1.234
    },
    "device_lat": {
      "title": "Device Latitude",
      "description": "Latitude of where the device is located.",
      "type": "number",
      "example": 1.234
    },
    "timestamp": {
      "title": "Timestamp",
      "description": "Date and timestamp of the item scanning event. - This should follow RFC3339 (ISO 8601) format.",
      "type": "string",
      "format": "date-time",
      "example": "2019-10-12T07:20:50.52Z"
    },
    "event_type": {
      "title": "Event Type",
      "description": "The type of the event. E.g. 'washed'",
      "type": "string",
      "example": "washed",
      "maxLength": 50
    },
    "item_id": {
      "title": "Item Identity",
      "description": "The identifier of the item material that can be looked up from - the product database",
      "type": "string",
      "example": "ITM:112233",
      "maxLength": 50
    },
    "item_description": {
      "title": "Item Description",
      "description": "Text description of the item or material. E.g. “plastic bottle”",
      "type": "string",
      "example": "plastic bottle",
      "maxLength": 255
    },
    "party_id": {
      "title": "Party ID",
      "description": "Identifier of the party involved. The organisation and owner - identification of the device at a site",
      "type": "string",
      "example": "PTY:778855",
      "maxLength": 50
    },
    "party_description": {
      "title": "Party Description",
      "description": "Text description of the party involved. E.g. “Waste Management”",
      "type": "string",
      "example": "PTY:778855",
      "maxLength": 255
    },
    "bearer_id": {
      "title": "Bearer ID",
      "description": "Identifier of the bearer involved. ",
      "type": "string",
      "example": "PTY:778855",
      "maxLength": 50
    },
    "bearer_descripiton": {
      "title": "Bearer ID",
      "description": "Text description of the bearer id. E.g. “Loyalty Card”",
      "type": "string",
      "example": "PTY:778855",
      "maxLength": 255
    }
  },
  "required": [
    "device_id",
    "device_lng",
    "device_lat",
    "timestamp",
    "event_type",
    "item_id"
  ]
}
```