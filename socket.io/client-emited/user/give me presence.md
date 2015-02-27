### give me presence(ack)
Returns contacts online/offline state.

Error types:
  - `something went wrong`

```javascript
presence = {
  15: false
  , 16: true
  , 17: false
}
```
Keys of hash are users ids and values are `isOnline` presenter (true → online, false → offline).
