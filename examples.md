# Event Examples

> Examples of how to use the event format

### Example Event JSON

```json
{
   "device_id": "DID:2222",
   "device_lng": 1.123,
   "device_lat": 52.123,
   "timestamp": "2022-06-16T15:34:58Z",
   "event_type": "make",
   "item_id": "item1",
   "item_description": "Optional description",
   "party_id": "OPTIONAL:123"
}
```
### Example POST Request

```sh
curl --location --request POST 'https://TOPO_API_DOMAIN/event' \
--header 'Authorization: Bearer <<TOKEN>> \
--header 'Content-Type: application/json' \
--data-raw '{
    "device_id": "DID:2222",
    "device_lng": 1.123,
    "device_lat": 52.123,
    "timestamp": "2022-06-16T15:34:58Z",
    "event_type": "make",
    "item_id": "item1",
    "item_description": "Optional description",
    "party_id": "OPTIONAL:123"
}'
```

Replace `<<TOKEN>>` with the API token issued by topolytics.
