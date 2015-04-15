### userlink update(data)
```javascript
data = {
  user_id : {integer}
  date    : {timestamp}
  status  : {string}('received'|'rejected'|'withdrawn')
}
```

После получения пакета необходимо обновить данные контакта %user% с id = data.user_id
```javascript
%user%.link_status = data.status
%user%.last_message_date = data.date
%user%.last_message = ''
%user%.first_name = ''
%user%.last_name = ''
%user%.avatar = ''
```
