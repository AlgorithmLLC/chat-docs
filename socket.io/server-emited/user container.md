### user container(container)

```javascript
data = {
  user       : [user]
  dialogs    : [dialog*]
  messages   : [message*]
}
```

[Описание объекта user](/object-types/user.md)

[Описание объекта dialog](/object-types/group.md)

[Описание объекта message](/object-types/dialog.md)

После получения пакета необходимо 

1. добавить/обновить данные контакта data.user.

2. добавить/обновить данные диалогов data.dialogs.

3. добавить/обновить данные сообщений data.messages.
