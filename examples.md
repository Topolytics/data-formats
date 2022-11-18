# Event Examples

> Examples of how to use the event format

### Example Event JSON

```json
{
   "device_id": "DID:2222",
   "device_coords": "123.54,45.5",
   "timestamp": "2022-06-16T15:34:58Z",
   "event_type": "yyyy",
   "item_id": "item1"
}
```

### Example POST Request

```json
curl --location --request POST 'https://events.dev.tp0.uk/event' \
--header 'Authorization: Bearer <<TOKEN>> \
--header 'Content-Type: application/json' \
--data-raw '{
    "device_id": "DID:2222",
    "device_coords": "123.54,45.5",
    "timestamp": "2022-06-16T15:34:58Z",
    "event_type": "yyyy",
    "item_id": "item1"
}'
```

Replace `<<TOKEN>>` with the API token issued by topolytics.
