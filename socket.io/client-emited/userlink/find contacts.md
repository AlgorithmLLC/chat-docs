### find contacts(search, ack)
```javascript
search = {
  search: {string}
}
```
Users global search.

Server returns:
```javascript
data = [
  {search_result_item}*
]
```
```javascript
search_result_item = {
  id        : {integer}, // found user id
  username  : {string},  // found user username
  domain_id : {integer}  // found user domain_id
}
```

Error types:
  - `something went wrong`
