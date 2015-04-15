### handle userlink(actionObject, ack)
```javascript
actionObject = {
  from_user_id : {integer}
  to_user_id   : {integer}
  action       : {string}('request'|'accept'|'reject'|'withdraw'|'remove'|'read')
}
```

#### request
Отправить запрос на добавление в список контактов.

Ответ сервера:<br />
```javascript
result = {
  user       : {user}      // without 'first_name', 'second_name', 'avatar'
  dialogs    : [{dialog}*]
  messages   : [{message}*]
}
```

#### accept
Одобрить запрос

Ответ сервера:<br />
```javascript
result = {
  user       : {user}
  dialogs    : []
  messages   : []
}
```

#### reject
Отклонить запрос

Ответ сервера:<br />
```javascript
result = 'success'
```

#### withdraw
Разорвать авторизацию

Ответ сервера:<br />
```javascript
result = 'success'
```

#### remove
Удалить из списка контактов

Ответ сервера:<br />
```javascript
result = 'success'
```

#### read
Сделать отметку о прочтении статуса авторизации


Ответ сервера:<br />
```javascript
result = 'success'
```


__Сообщения об ошибках__

`'something went wrong'`
