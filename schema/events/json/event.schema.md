## Event Schema

> Event Details

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
      "example": "DID:12345"
    },
    "device_lng": {
      "title": "Device Longitude",
      "description": "Longitude of where the device is located.",
      "type": "number",
      "example": 1.234
    },
    "device_lat": {
      "title": "Device Location Latitude",
      "description": "Latitude of where the device is located.",
      "type": "number",
      "example": 1.234
    },
    "timestamp": {
      "title": "Timestamp",
      "description": "Date and timestamp of the item scanning event. - The timestamp is in the following UTC format yyyy-mm-dd HH:MM:SS",
      "type": "string",
      "example": "06/11/2020 15:51:50 UTC"
    },
    "event_type": {
      "title": "Event Type",
      "description": "TBD",
      "type": "string",
      "example": "TBD"
    },
    "item_id": {
      "title": "Item Identity",
      "description": "The identifier of the item material that can be looked up from - the product database",
      "type": "string",
      "example": "ITM:112233"
    },
    "item_description": {
      "title": "Item Description",
      "description": "Text description of the item or material. E.g. “plastic bottle”",
      "type": "string",
      "example": "plastic bottle"
    },
    "party_id": {
      "title": "Party ID",
      "description": "Identifier of the party involved. The organisation and owner - idenfication of the device at a site",
      "type": "string",
      "example": "PTY:778855"
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