## File server
One of parts of chat backends is file server. It's used as store for message attachments and user avatars.

Client app gets file server config on [Data gathering](/basic-principes.md#data-gathering) step.

Incoming frame `storage urls` (client app not requests it, just listens. This behaviour will change):
```javascript
storage urls = {
  "get": "http://file-server.birdex.org/file/get/id/"
  ,"put": "http://file-server.birdex.org/file/put/id/"
  ,"putRaw": "http://file-server.birdex.org/file/putRaw/id/"
  ,"delete": "http://file-server.birdex.org/file/delete/id/"
}
```

Uuid is UUIDv4.
File uuid is required and must be contatinated to url as follows:
```
Action URL = storage url + avatar/attachment uuid.
```

### get
Get file.
- Request method: GET
- Parameters: no

### put
Deprecated. Put file.
- Request method: POST
- Parameters:
  - `body` — payload

### putRaw
Put file.
- Request method: POST
- Parameters: no
- Attachment or user avatar must be sent as request payload.

### delete
Delete file.
- Request method: GET
- Parameters: no
