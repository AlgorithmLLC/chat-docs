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

#### accept
Одобрить запрос

#### reject
Отклонить запрос

#### withdraw
Разорвать авторизацию

#### remove
Удалить из списка контактов

#### read
Сделать отметку о прочтении статуса авторизации
