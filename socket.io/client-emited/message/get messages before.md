### get messages before(filter, ack)
```javascript
filter = {
  last_date: "2014-11-24 06:21:24"
  , first_date: "2014-11-24 06:21:24" // optional
  , dialog_id: 15
  , limit: 30 // optional

}
```
Get messages for dialog for specified filter.

Filtering: return messages for query
```SQL
WHERE
  message.created_at >= (first_date !== null ? first_date : '1970-01-01')
  AND
  message.created_at <= last_date
LIMIT (limit ? limit : Infinity)
```

Error types:
  - `something went wrong`

Returns array of `message object`s.
